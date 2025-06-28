<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
</head>
<body>

  <script>
   
    function generujParzyste(ile = 200) {
      const tab = [];
      while (tab.length < ile) {
        let liczba = Math.floor(Math.random() * 1000);
        if (liczba % 2 === 0) tab.push(liczba);
      }
      return tab;
    }

    
    function sumaCiagu(n) {
      return (n * (n + 1)) / 2;
    }

  
    function resztaZDzielenia(a, b) {
      return a % b;
    }

    
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

    function sredniaTrzech(a, b, c) {
      return (a + b + c) / 3;
    }


    console.log("Zadanie 3a - Parzyste liczby (200):", generujParzyste());
    console.log("Zadanie 3b - Suma ciągu od 1 do 10:", sumaCiagu(10));
    console.log("Zadanie 3c - Reszta z dzielenia 17 % 5:", resztaZDzielenia(17, 5));

    console.log("Zadanie 4a - Liczby pierwsze (200):", generujPierwsze());
    console.log("Zadanie 4b - Średnia z 5, 10, 15:", sredniaTrzech(5, 10, 15));
  </script>

</body>
</html>



function generujNieparzyste(ile = 200) {
  const tab = [];
  while (tab.length < ile) {
    let liczba = Math.floor(Math.random() * 1000);
    if (liczba % 2 !== 0) tab.push(liczba);
  }
  return tab;

// ZADANIE 12
// var jeden = prompt("Wprowadź pierwszą liczbę:");
// var dwa = prompt("Wprowadź drugą liczbę:");
// jeden =Number(jeden) 
// dwa = Number(dwa);
// dwa

// if (jeden == dwa)
//     alert(" jest równe ");
// else{   
//         if (jeden<dwa)
//             alert(jeden+" jest mniejsze niż "+dwa);
//         else
//         alert(jeden+" jest większe niż "+dwa);
//     }


// ZADANIE 13
// function wypelnijLosowymi(n=100){
//     tablica =[];
//     for (i = 0; i < n; i++) {
//         tablica.push(Math.round(Math.random() * 10));
//     }
//     return tablica
// }

// tab =  wypelnijLosowymi(10)
// console.log(tab)

// var liczba = prompt("Wprowadź pierwszą liczbę:");

// count = 0
// for (i = 0; i <tab.length; i++) {
//     if(tab[i] == liczba)
//         count++
//     }
//     console.log(count)

// ZADANIE 14
// tab = [1,2,3,4,5,6]

// a = tab.slice(0, 3);
// b = tab.slice(3, 5);
// a.push(77)

// console.log(a)
// console.log(a.concat(b))


//////////////////// ciagi

1. Ciąg naturalny (1, 2, 3, 4, 5...)

function ciagNaturalny(n) {
  let wynik = "";
  for (let i = 1; i <= n; i++) {
    wynik = wynik + i + " ";
  }
  console.log(wynik);
}
3. Ciąg nieparzystych (1, 3, 5, 7, 9...)

function ciagNieparzystych(n) {
  let wynik = "";
  for (let i = 1; i <= n; i++) {
    wynik = wynik + (2 * i - 1) + " ";
  }
  console.log(wynik);
}
4. Ciąg kwadratów (1, 4, 9, 16, 25...)

function ciagKwadratow(n) {
  let wynik = "";
  for (let i = 1; i <= n; i++) {
    wynik = wynik + (i * i) + " ";
  }
  console.log(wynik);
}
10. Ciąg od 1 do 10

function ciagDo10() {
  let wynik = "";
  for (let i = 1; i <= 10; i++) {
    wynik = wynik + i + " ";
  }
  console.log(wynik);
}
