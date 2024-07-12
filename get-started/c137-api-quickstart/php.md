---
description: This quickstart shows you how to get started with the C137 API using the PHP.
---

# 🐘 PHP

## Quickstart

### Steps:

1. Obtain your API key: Visit the C137 Console to obtain your unique API key.
2. Make API requets:

```php
<?php

// Substitua "YOUR_API_KEY" pela sua chave API real
$URL = "https://c137.belini.shop/api/generateText";
$KEY = "YOUR_API_KEY";

$data = [
    "key" => $KEY,
    "text" => "List 5 big countries.",
];

$ch = curl_init($URL);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_POST, true);
curl_setopt($ch, CURLOPT_POSTFIELDS, http_build_query($data));

$response = curl_exec($ch);
$status_code = curl_getinfo($ch, CURLINFO_HTTP_CODE);
curl_close($ch);

echo "Status: " . $status_code . PHP_EOL;

echo "------------------------------------------" . PHP_EOL;
echo $response . PHP_EOL;
echo "------------------------------------------" . PHP_EOL;

?>
```
