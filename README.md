# c-dz0
Nulta zadaca za c# vjestinu

#1191228769

#Pitanje 1:

U debug folder za konzolnu aplikaciju su dodani .dll i .pdb fajlovi od ClassLibrary projekta. 
Ako maknem .dll za library iz foldera i probam pokrenuti aplikaciju, odmah dolazi do rusenja, 
    a konzola javlja za 'unhandled FileNotFoundException'. To je zato sto pokusava pokrenuti
    MyConsole.PrintHelloWorld metodu, cija je implementacija u nestaloj .dll datoteci. 
Kada bih vam slao aplikaciju, poslao bih vam kompletan sadrzaj bin/Debug foldera. 

#Pitanje 2:

Aplikacija je koristila staru verziju asemblija, jer .exe ne biva azuriran prije nego sto compiliramo
    solution. 

#Pitanje 3: 

Pero: Hello World

#Pitanje 4: 

Dodan je PeroClassLibrary.dll, ali ne i .pdb.

#Pitanje 5:

Build is aplikacija i dalje rade jer je izvorni .dll bio kopiran u folder projekta. Aplikacija i 
    Visual Studio nikad nije zanimala originalna datoteka - samo ona koja je bila kopirana. 
    Tocnije receno, VS je jedino pogledao originalnu datoteku prilikom dodavanja reference, tada ju
    je kopirao i daljle koristio svoju verziju.

#Pitanje 6: 

packages direktorij ponovno je generiran/skinut kao dio build procesa. Sam proces prolazi bez greske i bez
    ocitog smanjenja brzine. 