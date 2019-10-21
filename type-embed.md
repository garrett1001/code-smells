```php
$queryGrid = "
  SELECT COUNT(*) AS count,idLocation AS id
  FROM locations
  WHERE longitude = :long AND latitude = :lat";
```