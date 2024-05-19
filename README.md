Leírás:

Egy olyan weboldalt készítettem, amely az oldal újratöltése nélkül képes új tartalmakat betölteni AJAX segítségével.
A navigációs gombok megnyomásával a különböző HTML fájlok tartalmai töltődnek be az oldal tartalom részébe. Sajnos időhiány miatt nem úgy néz ki mint amit elterveztem de remélem a kritériumokat teljesítettem.
A betöltést úgy oldottam meg, hogy minden nav gombra feliratkoztattam egy event listener-t. Az event listener azt csinálja, hogy kiveszi a jelenleg active navlink osztályából (ha van) az active-t.
Ez azért kell, mivel az lesz az új active amire éppen kattintottunk. Az eltávolítást követően a kattintott linknek az osztályához hozzáadjuk az active osztályt és ezt követően egy külön kiszervezett
függvényben betöltjük a html fájlt. A betöltés abból áll, hogy a tabcontent-nek az innerHTML-jét beállítjuk a másik fájl tartalmára XMLHttpRequest segítségével. A betöltést követően az active osztályt
hozzáadjuk a kattintott navlink-hez.

Az oldal futtatásához muszáj volt a vscode-ban letöltenem a Live Server extension-t, mivel csak az index.html futtatásával nem működik az XMLHttpRequest.
