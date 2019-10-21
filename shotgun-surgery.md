## Shotgun Surgery

If the Address class were changed in anyway, it will affect both the Photographer and User class, since Client class have an address field extended from the Address class.
```python
class Address(models.Model):
   country_sn = models.TextField()
   state_sn = models.TextField()
   city_sn = models.TextField()
   latitude = models.DecimalField(max_digits = 9, decimal_places = 6)
   longitude = models.DecimalField(max_digits = 9, decimal_places = 6)
   def __str__(self):
       return self.city_sn + ", " + self.state_sn + ", " + self.country_sn

data = {
          "photographers" : Photographer.objects.all().filter(client__address__longitude = longitude, client__address__latitude = latitude),
          "lat" : latitude,
          "lng" : longitude
      }
```