## Conditional Complexity

Tripple nested if statments increase the cyclomatic complexcity of this function
```python
def login_user(request):
    if request.method == "POST":
        email = request.POST['email']
        password = request.POST['password']
        username = get_user(email)
        user = authenticate(username=username, password=password)
        if user is not None:
            if user.is_active:
                login(request, user)
                return redirect('/')
            else:
                return render(request, 'usermanagement/login.html', {'loginerror': True})
        else:
            return render(request, 'usermanagement/login.html', {'loginerror': True})
    elif request.user.is_authenticated:
        return redirect('/')
    else:
        return render(request, 'usermanagement/login.html')
```

In our example, we have an if statement that checks a file extension. We use it to avoid animated files that aren't images. Since we may come across more file extensions in the future that we want to ignore, or potentially brand new file extensions, a better solution would be putting all the extensions in a list rather than a long one-line.

```{python}
 if fextension != ".gif" and fextension != ".mp4" and fextension != ".mov" and fextension != ".flv" and fextension != ".gifv":
```

