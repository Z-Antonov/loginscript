# Loginscript 
Dies ist ein simpler Loginscript inklusive Registrierung und internem Bereich. Eine ausführliche Dokumentation und Schritt-für-Schritt-Anleitung ist auf [PHP-Einfach.de - Loginscript](http://www.php-einfach.de/experte/php-codebeispiele/loginscript/) zu finden. 

**Download**: [.zip](https://github.com/PHP-Einfach/loginscript/archive/master.zip) 

## Installation
Nach dem Download des [ZIP-Archives](https://github.com/PHP-Einfach/loginscript/archive/master.zip) müsst ihr zuerst die notwendige Datenbanktabelle erstellen. Die SQL-Befehle findet ihr in der Datei `users.sql` oder alternativ führt die folgenden SQL-Befehle in z.B. phpMyAdmin aus:

```sql
CREATE TABLE IF NOT EXISTS `users` (
  `id` int(10) unsigned NOT NULL AUTO_INCREMENT,
  `email` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `passwort` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `vorname` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `nachname` varchar(255) COLLATE utf8_unicode_ci NOT NULL,
  `created_at` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `updated_at` timestamp NULL DEFAULT NULL,
  `passwortcode` varchar(255) COLLATE utf8_unicode_ci DEFAULT NULL,
  `passwortcode_time` timestamp NULL DEFAULT NULL,
  PRIMARY KEY (`id`), UNIQUE (`email`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;
```


Als nächsten Stritt müsst ihr die Verbindungsdaten zu eurer Datenbank anpassen. Öffnet dazu die `inc/config.inc.php` und tragt dort den Benutzernamen, das Passwort, und den Datenbanknamen eurer MySQL-Datenbank ein.

## Screenshots
### Startseite:
![Index](/screenshots/index.png)

### Registrierung:
![Registrierung](/screenshots/registrierung.png)

### Interner Bereich (nach erfolgreichem Login):
![Interner Bereich](/screenshots/interner_bereich.png)


## Webhosting
Falls ihr auf der Suche nach günstigen Webhosting für euren Login-Script, kann ich euch die Webhosting-Angebote von netcup empfehlen. Preis pro Monat beginnt ab 1,99 Euro für vollwertigen Webspace. Mit den Gutscheinen von [www.netcupgutscheine.de](http://www.netcupgutscheine.de) könnt ihr ebenfalls nochmal 5 Euro sparen.
