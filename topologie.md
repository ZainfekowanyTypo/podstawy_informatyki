# Topologie Sieci

## Sieci Fizyczne
Sieci fizyczne odnoszą się do fizycznego ułożenia kabli, urządzeń i połączeń. Przykłady:
- **Topologia magistrali** (Bus) : jest to podłączenie wszystkich urządzeń do jednej magistrali, która przekazuje między nimi dane.
  - Wady: Ograniczona przepustowość, w przypadku awarii, cała sieć może przestać działać, a sam błąd cięzko zdiagnozować. 
  - Zalety: Jest bardzo prosta w użyciu i tania, co pozwala na szybką instalacje. 
  - Gdzie stosowane: Nadaję się najlepiej do małych sieci LAN, szczególnie w domach.
- **Topologia pierścienia** (Ring): Każde urządzenie jest połączone z dwoma innymi, tworząc "zamknięty pierścień". Dane podróżują wokół pierścienia, aż dotrą do wybranego celu. W tej topologii używa się tokenów, czyli pakietów które nadają dostęp do nadawania danych.
  - Wady: Cała sieć przestaje działać w przypadku awarii jednego urządzenia o ile nie zastosowano redundancji, występują opóźnienia przesyłania danych, poniewaz dane muszą przejść przez wszystkie urządzenia sieci.
  - Zalety: Łatwo można kontrolować, które urządzenie ma dostęp do medium, dzięki tokenom. 
  - Gdzie stosowane: Sieci LAN w korporacjach, które korzystają z protokołu Token Passing.
- **Topologia gwiazdy** (Star): Podłączenie wszystkich urządzeń w sieci z jednym centralnym urządzeniem. Urządzenie łaczą się ze sobą poprzez centralny punkt.
  - Wady: Sieć przestaje działać w przypadku awarii centralnego koncentratora, nie jest tania.
  - Zalety: Awaria tylko jednego szczególnego urządzenia powoduje nie działanie sieci, łatwo równiez sieć rozbudować i diagnozować.
  - Gdzie stosowane: Idealna w biurach, szkołach i korporacjach.


## Sieci Logiczne
Sieci logiczne opisują sposób przesyłania danych między urządzeniami, niezależnie od fizycznej struktury. Przykłady:
- **Punkt-punkt** (Point-to-Point): jest to komunikacja bezpośrednio między dwoma urządzeniami.
  - Wady: Aby podłączyć kolejne urządzenie, trzeba stworzyć nowe połączenie.
  - Zalety: Łatwo skonfigurować połączenie między dwoma urządzeniami, opóźnienia i straty są minimalne.
  - Zastosowanie: Używane do połączeń między dwoma urządzeniami, np. komputerem a drukarką, lub w połączeniach między routerami.
- **Przekazywanie żetonu** (Token Passing): urządzenie posiadające specjalny token może nadawać dane.
  - Wady: Token musi przejść przez wszystkie urządzenia, co może powodować opóźnienia i zarządzanie tokenem jest czasami skomplikowane.
  - Zalety: Ponieważ tylko jedno urządzenie może nadawać w danym momencie, unika się kolizji, sieć działa sprawnie.
  - Zastosowanie: Sieci oparte na topologii pierścienia, zwłaszcza w większych organizacjach, które wymagają efektywnej kontroli dostępu
- **Wielodostępowa** (Multiple Access): wiele urządzeń współdzieli medium transmisyjne.
  - Wady: Mogą występować kolizje, które zmniejszają efektywność sieci, w sieciach o dużym natężeniu ruchu zarządzanie dostępem może być bardziej skomplikowane.
  - Zalety: Wiele urządzeń może korzystać z tego samego medium transmisyjnego, łatwo rozbudować sieć o nowe urządzenia.
  - Zastosowanie: Typowe dla sieci Ethernet i Wi-Fi