## Éviter les spam 

./classes/Mail.php
- Modifier Mail.php : ligne 468
```html
$subject = strip_tags($configuration['PS_SHOP_NAME']) . ' - ' . $subject;
```