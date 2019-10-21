## Inconsistent Names

Inconsistent in method naming. getLocation is in camel case, which get_email is in snake case.
```python
class Client(models.Model):
    user = models.OneToOneField(User, on_delete=models.CASCADE)
    address = models.ForeignKey(Address, on_delete=models.CASCADE, null=True)
    dob = models.DateField(null=False, blank=False)

    def getCity(self):
        return

    def getState(self):
        return

    def getCountry(self):
        return

    def getLocation(self):
        return

    def get_email(self):
        return self.user.email

    def __str__(self):
        return self.user.username
```