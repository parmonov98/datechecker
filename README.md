# datechecker
when u need to validate string coming from HTML from.

```
function dateCheck($date,$format='d/m/Y'){
    $parts = date_parse_from_format($format, $date);
    return (checkdate($parts['month'],$parts['day'],$parts['year'])) ? true : false;
}
$date = "04-01-1998";
echo (dateCheck($date,'d-m-Y')) ? "Date $date is true" : "Date $date is false";
$date2 = "18/09/2011";
echo (dateCheck($date2)) ? "Date $date2 is true" : "Date $date2 is false";
```
