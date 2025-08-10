# esp8266-weather-station-color-D1_mini 

(oryginalny kod ThingPulse, został zmodyfikowany w dużej mierze do moich wymagań i potrzeb )
Openweather zwraca opis pogody w j. ang. dodałem:

// implementacja funkcji removePolishAccents
String removePolishAccents(String text) {
  // Zamiana polskich ogonków na znaki bez ogonków
  text.replace("ą", "a");
  text.replace("Ą", "A");
  text.replace("ć", "c");
  text.replace("Ć", "C");
  text.replace("ę", "e");
  text.replace("Ę", "E");
  text.replace("ł", "l");
  text.replace("Ł", "L");
  text.replace("ń", "n");
  text.replace("Ń", "N");
  text.replace("ó", "o");
  text.replace("Ó", "O");
  text.replace("ś", "s");
  text.replace("Ś", "S");
  text.replace("ź", "z");
  text.replace("Ź", "Z");
  text.replace("ż", "z");
  text.replace("Ż", "Z");
  

ESP8266 Stacja pogodowa Color przy użyciu wyświetlacza TFT ILI9341 240x320, 2,8-calowy ekran dotykowy.
Ekran pokazuje lokalne warunki za pośrednictwem Open Weather Map. 
Główny ekran pokazuje czas, datę, aktualną pogodę, 7-dniową prognozę i fazę księżyca każdego dnia, a kolejne ekrany przechodzą w dalsze szczegóły.
![20250805_182314](https://github.com/user-attachments/assets/02174032-9463-4f57-b7f6-b365e462c812)

Pierwsze uruchomienie:
WiFiManager - utworzy AP - portal konfiguracyjny pod nazwą:

"StacjaPogodowa-Config"

WIFI_MANAGER_AP_PASSWORD "pogoda123"  // hasło do portalu konfiguracyjnego

![20250807_193353](https://github.com/user-attachments/assets/fdef8cc3-935c-4490-bf3f-2002abac6645)

![20250807_193357](https://github.com/user-attachments/assets/775f873a-420d-4d14-8d42-0de367ac226e)


![Screenshot_20250802_093250_Samsung Internet](https://github.com/user-attachments/assets/fdb19e37-43cb-4ea2-9162-8a804a8a6b8b)


Ustawienia pliku platformio.ini

![2025-08-10_085800](https://github.com/user-attachments/assets/488f10ad-ecf3-48a3-b0c9-00e887f627fd)

Schemat podłączenia esp8266 z ILI9341, dostępny w pliku "\src\resources\PlaneSpotterWiring.png"
