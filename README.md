<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <script>
    // Zadanie 3a: Losowe liczby parzyste
    function generujParzyste(ile = 200) {
      const tab = [];
      while (tab.length < ile) {
        let liczba = Math.floor(Math.random() * 1000);
        if (liczba % 2 === 0) tab.push(liczba);
      }
      return tab;
    }

    // Zadanie 3b: Suma ciągu 1+2+...+n
    function sumaCiagu(n) {
      return (n * (n + 1)) / 2;
    }

    // Zadanie 3c: Reszta z dzielenia
    function resztaZDzielenia(a, b) {
      return a % b;
    }

    // Zadanie 4a: Liczby pierwsze
    function czyPierwsza(n) {
      if (n < 2) return false;
      for (let i = 2; i <= Math.sqrt(n); i++) {
        if (n % i === 0) return false;
      }
      return true;
    }

    function generujPierwsze(ile = 200) {
      const liczby = [];
      let liczba = 2;
      while (liczby.length < ile) {
        if (czyPierwsza(liczba)) {
          liczby.push(liczba);
        }
        liczba++;
      }
      return liczby;
    }

    // Zadanie 4b: Średnia trzech liczb
    function sredniaTrzech(a, b, c) {
      return (a + b + c) / 3;
    }

    // --- Wypisywanie wyników do konsoli ---
    console.log("Zadanie 3a - Parzyste liczby (200):", generujParzyste());
    console.log("Zadanie 3b - Suma ciągu od 1 do 10:", sumaCiagu(10));
    console.log("Zadanie 3c - Reszta z dzielenia 17 % 5:", resztaZDzielenia(17, 5));

    console.log("Zadanie 4a - Liczby pierwsze (200):", generujPierwsze());
    console.log("Zadanie 4b - Średnia z 5, 10, 15:", sredniaTrzech(5, 10, 15));
  </script>

</body>
</html>
