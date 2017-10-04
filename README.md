# Herzlich Willkommen

Wir haben hier für dich eine online Version des Cheat Sheet's, der Vorteil der webbasierten Umgebung, welche wir hier besitzen, sie haben ein Benutzerfreundliches GUI, sprich sie haben ein Code Highlighting.


### Inhaltsverzeichnis

1. Arrays
1.1 Arrays definieren
1.2 Arrays ausgeben
1.3 Assoziative Arrays
1.4 Array erweitern
2. Vordefinierte Systemvariablen
2.1 Variablen für den Zugriff auf HTML Parameter
2.2 Allgemeine Systeminformationen
3. Funktionen zur Arraybearbeitung
3.1 Arrayzeiger
3.2 Arrayfunktionen
3.3 Arrays verknüpfen
3.4 Arrays sortieren


# 1. Arrays

## 1.1 Array definieren

In einem Array können sie nun beliebig viele Werte speichern, auch von unterschiedlichen Typen. So kann ein PHP-Array z.B. eine Zeichenkette String, eine Zahl mit Kommastellen oder eine Ganzzahl enthalten. 

Hier wird nun ein Array definiert, $wochentag soll der Namen des Arrays werden, mittels der array() -Funktion werden nun Werte in den Array geschrieben. 

```php
<?php
$wochentage = array("Sonntag","Montag","Dienstag","Mittwoch","Donnerstag","Freitag","Samstag");
?>
```

## 1.2 Array ausgeben

Das ausgeben des eben erst erstellten Arrays ist relativ simpel, dazu erstellen wir einen echo und geben anschliessend den Namen unseres Arrays an, wenn sie nun gezielt nach einem Index-Wert suchen wollen, können sie dies auch machen, indem sie einfach nach dem Array-Namen noch den Index-Wert angeben. 

```php
<?php
$wochentage = array("Sonntag","Montag","Dienstag","Mittwoch","Donnerstag","Freitag","Samstag");

echo $wochentage[1];

?>
```

## 1.3 Assoziative Arrays

Wenn sie nun ein grösseres Array haben, wird es irgendwann immer mühsamer, zu wissen, welche Index-Nummer das gewünschte Element hat, darum gibt es nun Hilfe mit dem sogenannten assoziativen Array. Das heisst man kann für einen Wert einen Key festlegen, diese Wert-Zuweisung erfolgt über => 

```php
<?php
$wochentage = array(
"so" => "Sonntag",
"mo" => "Montag",
"di" => "Dienstag",
"mi" => "Mittwoch",
"do" => "Donnerstag",
"fr" => "Freitag",
"sa" => "Samstag");

echo $wochentage["mo"];
?>
```

## 1.4 Array erweitern

Ein Array kann bequem erweitert werden, bzw. neue Werte dem Array mitgegeben werden. Die funktioniert nun indem wir den Arraynamen angeben und gleich nach dem Namen diese – [] – Klammern einsetzen. 

```php
<?php
$mitarbeiter = array("Bob","Peter");
$mitarbeiter[] = "Lisa";

echo $mitarbeiter[2];
?>
```


# 2. Vordefinierte Systemvariablen

PHP stellt verschiedene global erreichbare Systemvariablen zu Verfügung. 

## 2.1 Variablen für den Zugriff auf HTML Parameter

Jedes PHP-Skript hat Zugriff auf die drei Variablen $_POST, $_GET und $_REQUEST. Diese drei Variablen enthalten Werte, welche an das Skript übergebene Werte enthalten.

## 2.2 Allgemeine Systeminformationen

Name der momentan geöffneten Datei
echo $_SERVER["PHP_SELF"]; 

Name des Servers
echo $_SERVER["SERVER_NAME"]; 

Name und Version des Zugangsprotokolls  
echo $_SERVER["SERVER_PROTOCOL"]; 

Der Query String, falls vorhanden 
echo $_SERVER["QUERY_STRING"]; 

Zeigt das Document-Root an, wie es in der Konfigurationsdatei des Webservers definiert ist 
echo $_SERVER["DOCUMENT_ROOT"]; 

Adresse die auf die aktuelle Seite verwiesen hat
echo $_SERVER["HTTP_PREFER"]; 

Name resp. Kennung des Browserbesuchers
echo $_SERVER["HTTP_USER_AGENT"]; 

IP-Adresse des Besuchers
echo $_SERVER["REMOTE-ADDR"]; 

Port der verwendet wird, um mit dem Webserver zu kommunizieren
echo $_SERVER["REMOTE_PORT"]; 

Port der vom Webserver verwendet wird, um mit dem Besucher zu kommunizieren
echo $_SERVER["SERVER_PORT"]; 


# 3. Funktionen zur Arraybearbeitung

## 3.1 Arrayzeiger

Jedes Element, welches mehr als eine Wert beinhaltet, besitzt einen Pointer (Zeiger), dieser zeigt im Array auf ein bestimmtes Element bzw. Wert. Dieser sogenannte Pointer ist nun vergleichbar mit einem Wegweiser. 

## 3.2 Arrayfunktionen

PHP bietet mehr als 50 Funktionen im Zusammenhang mit Arrays an, diese können sie online konsultieren.

 [Sehen sie mehr Funktionen](http://php.net/manual/de/ref.array.php).

## 3.3 Arrays verknüpfen

Sie können mittels der Funktion array_merge() mehrere Arrays miteinander verknüpfen. 

```php
<?php
$array1 = array(3, 2, 4);
$array2 = array("a", "b", "c");
$ergebnis = array_merge($array1, $array2);

print_r($ergebnis);
?>
```

## 3.4 Arrays sortieren

Arrays können sie mit der Funktion sort() sortiert werden, ebenfalls können sie bestimmen ob von A nach Z oder von Z nach A sortiert werden soll, also auf oder absteigend. 

```php
<?php
$namen = array("Klaus", "Dieter", "Anna", "Melissa", "Peter");

sort($namen);
?>
```


# 4. Quellen

1. Buch (Schooltas.net)
2. [Arrays](http://php.net/manual/de/language.types.array.php)
