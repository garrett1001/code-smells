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