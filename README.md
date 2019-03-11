print() Fonksiyonu
Geçen bölümde bir yandan Python’ın etkilesimli kabugunu yakından tanıyıp bu vesileyle bazı
önemli fonksiyon ve araçları ögrenirken, öbür yandan bu ögrendiklerimizi kullanarak örnek
programlar yazdık. Gördügünüz gibi, azıcık bir bilgiyle dahi az çok ise yarar programlar
yazmak mümkün olabiliyor. Daha yararlı programlar yazabilmek için henüz ögrenmemiz
gereken pek çok sey var. Iste bu bölümde, ‘daha yararlı programlar yazmamızı’ saglayacak
çok önemli bir araçtan söz edecegiz. Öneminden dolayı ayrıntılı bir sekilde anlatacagımız bu
aracın adı print() fonksiyonu.
Elbette bu bölümde sadece print() fonksiyonundan bahsetmeyecegiz. Bu bölümde print()
fonksiyonunun yanısıra Python’daki bazı önemli temel konuları da ele alacagız. Mesela bu
bölümde Python’daki karakter dizilerine ve sayılara iliskin çok önemli bilgiler verecegiz. Ayrıca
print() fonksiyonu vesilesiyle Python’daki ‘fonksiyon’ konusuna da saglam bir giris yapmıs,
bu kavram ile ilgili ilk bilgilerimizi almıs olacagız. Sözün özü, bu bölüm bizim için, deyim
yerindeyse, tam anlamıyla bir dönüm noktası olacak.
O halde isterseniz lafı daha fazla uzatmadan ise print() fonksiyonunun ne oldugu ve ne ise
yaradıgını anlatarak baslayalım.
Nedir, Ne Ise Yarar?
Simdiye kadar etkilesimli kabukta gerek karakter dizilerini gerekse sayıları dogrudan ekrana
yazdık. Yani söyle bir sey yaptık:
>>> "Python programlama dili"
'Python programlama dili'
>>> 6567
6567
Etkilesimli kabuk da, ekrana yazdıgımız bu karakter dizisi ve sayıyı dogrudan bize çıktı
olarak verdi. Ancak ilerde Python kodlarımızı bir dosyaya kaydedip çalıstırdıgımızda da
göreceginiz gibi, Python’ın ekrana çıktı verebilmesi için yukarıdaki kullanım yeterli degildir.
Yani yukarıdaki kullanım yalnızca etkilesimli kabukta çalısır. Bu kodları bir dosyaya kaydedip
çalıstırmak istedigimizde hiçbir çıktı alamayız. Python’da yazdıgımız seylerin ekrana çıktı
olarak verilebilmesi için print() adlı özel bir fonksiyondan yararlanmamız gerekir.
O halde gelin bu print() fonksiyonunun ne ise yaradıgını ve nasıl kullanıldıgını anlamaya
çalısalım:
50
Python 3 için Türkçe Kılavuz, Sürüm 3
print() de tıpkı daha önce gördügümüz type(), len() ve pow() gibi bir fonksiyondur.
Fonksiyonları ilerde daha ayrıntılı bir sekilde inceleyecegimizi söylemistik hatırlarsanız. O
yüzden fonksiyon kelimesine takılarak, burada anlattıgımız seylerin kafanızı karıstırmasına,
moralinizi bozmasına izin vermeyin.
print() fonksiyonunun görevi ekrana çıktı vermemizi saglamaktır. Hemen bununla ilgili bir
örnek verelim:
>>> print("Python programlama dili")
Python programlama dili
Bildiginiz gibi burada gördügümüz “Python programlama dili” bir karakter dizisidir. Iste
print() fonksiyonunun görevi bu karakter dizisini ekrana çıktı olarak vermektir. Peki
bu karakter dizisini print() fonksiyonu olmadan yazdıgımızda da ekrana çıktı vermis
olmuyor muyuz? Aslında olmuyoruz. Dedigimiz gibi, ilerde programlarımızı dosyalara
kaydedip çalıstırdıgımızda, basında print() olmayan ifadelerin çıktıda görünmedigine sahit
olacaksınız.
Daha önce de dedigimiz gibi, etkilesimli kabuk bir test ortamı olması açısından rahat bir
ortamdır. Bu sebeple bu ortamda ekrana çıktı verebilmek için print() fonksiyonunu
kullanmak zorunda degilsiniz. Yani basında print() olsa da olmasa da etkilesimli kabuk
ekrana yazdırmak istediginiz seyi yazdırır. Ama iyi bir alıskanlık olması açısından, ekrana
herhangi bir sey yazdıracagınızda ben size print() fonksiyonunu kullanmanızı tavsiye
ederim.
print() son derece güçlü bir fonksiyondur. Gelin isterseniz bu güçlü ve faydalı fonksiyonu
derin derin incelemeye koyulalım.
Nasıl Kullanılır?
Yukarıda verdigimiz örnekte ilk gözümüze çarpan sey, karakter dizisini print()
fonksiyonunun parantezleri içine yazmıs olmamızdır. Biz bir fonksiyonun parantezleri içinde
belirtilen ögelere ‘parametre’ dendigini geçen bölümde ögrenmistik. Tıpkı ögrendigimiz öteki
fonksiyonlar gibi, print() fonksiyonu da birtakım parametreler alır.
Bu arada print() fonksiyonunun parantezini açıp parametreyi yazdıktan sonra, parantezi
kapatmayı unutmuyoruz. Python programlama diline yeni baslayanların, hatta bazen
deneyimli programcıların bile en sık yaptıgı hatalardan biri açtıkları parantezi kapatmayı
unutmalarıdır.
Elbette, eger istersek burada dogrudan “Python programlama dili” adlı karakter dizisini
kullanmak yerine, önce bu karakter dizisini bir degiskene atayıp, sonra da print()
fonksiyonunun parantezleri içinde bu degiskeni kullanabiliriz. Yani:
>>> dil = "Python programlama dili"
>>> print(dil)
Python programlama dili
Bu arada, hem simdi verdigimiz, hem de daha önce yazdıgımız örneklerde bir sey dikkatinizi
çekmis olmalı. Simdiye kadar verdigimiz örneklerde karakter dizilerini hep çift tırnakla
gösterdik. Ama aslında tek seçenegimiz çift tırnak degildir. Python bize üç farklı tırnak
seçenegi sunar:
6.2. Nasıl Kullanılır? 51
Python 3 için Türkçe Kılavuz, Sürüm 3
1. Tek tırnak (‘ ‘)
2. Çift tırnak (” ”)
3. Üç tırnak (“”” “””)
Dolayısıyla yukarıdaki örnegi üç farklı sekilde yazabiliriz:
>>> print('Python programlama dili')
Python programlama dili
>>> print("Python programlama dili")
Python programlama dili
>>> print("""Python programlama dili""")
Python programlama dili
Gördügünüz gibi çıktılar arasında hiçbir fark yok.
Peki çıktılarda hiçbir fark yoksa neden üç farklı tırnak çesidi var?
Isterseniz bu soruyu bir örnek üzerinden açıklamaya çalısalım. Diyelim ki ekrana söyle bir
çıktı vermek istiyoruz:
Python programlama dilinin adı "piton" yılanından gelmez
Eger bu cümleyi çift tırnaklar içinde gösterirsek programımız hata verecektir:
>>> print("Python programlama dilinin adı "piton" yılanından gelmez")
File "<stdin>", line 1
print("Python programlama dilinin adı "piton" yılanından gelmez")
^
SyntaxError: invalid syntax
Bunun sebebi, cümle içinde geçen ‘piton’ kelimesinin de çift tırnaklar içinde gösterilmis
olmasıdır. Cümlenin, yani karakter dizisinin kendisi de çift tırnak içinde gösterildigi için
Python, karakter dizisini baslatan ve bitiren tırnakların hangisi oldugunu ayırt edemiyor.
Yukarıdaki cümleyi en kolay su sekilde ekrana yazdırabiliriz:
>>> print('Python programlama dilinin adı "piton" yılanından gelmez')
Python programlama dilinin adı "piton" yılanından gelmez
Burada karakter dizisini tek tırnak içine aldık. Karakter dizisi içinde geçen ‘piton’ kelimesi
çift tırnak içinde oldugu için, karakter dizisini baslatıp bitiren tırnaklarla ‘piton’ kelimesindeki
tırnakların birbirine karısması gibi bir durum söz konusu degildir.
Bir de söyle bir örnek verelim: Diyelim ki asagıdaki gibi bir çıktı elde etmek istiyoruz:
İstanbul'un 5 günlük hava durumu tahmini
Eger bu karakter dizisini tek tırnak isaretleri içinde belirtirseniz Python size bir hata mesajı
gösterecektir:
52 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> print('İstanbul'un 5 günlük hava durumu tahmini')
File "<stdin>", line 1
print('İstanbul'un 5 günlük hava durumu tahmini')
^
SyntaxError: invalid syntax
Bu hatanın sebebi ‘Istanbul’un’ kelimesi içinde geçen kesme isaretidir. Tıpkı bir önceki
örnekte oldugu gibi, Python karakter dizisini baslatan ve bitiren tırnakların hangisi oldugunu
kestiremiyor. Python, karakter dizisinin en basındaki tek tırnak isaretinin ardından
‘Istanbul’un’ kelimesi içindeki kesme isaretini görünce karakter dizisinin burada sona erdigini
zannediyor. Ancak karakter dizisini soldan saga dogru okumaya devam edince bir yerlerde
bir terslik oldugunu düsünüyor ve bize bir hata mesajı göstermekten baska çaresi kalmıyor.
Yukarıdaki karakter dizisini en kolay söyle tanımlayabiliriz:
>>> print("İstanbul'un 5 günlük hava durumu tahmini")
İstanbul'un 5 günlük hava durumu tahmini
Burada da, karakter dizisi içinde geçen kesme isaretine takılmamak için karakter dizimizi çift
tırnak isaretleri içine alıyoruz.
Yukarıdaki karakter dizilerini düzgün bir sekilde çıktı verebilmek için üç tırnak isaretlerinden
de yararlanabiliriz:
>>> print("""Python programlama dilinin adı "piton" yılanından gelmez""")
Python programlama dilinin adı "piton" yılanından gelmez
>>> print("""İstanbul'un 5 günlük hava durumu tahmini""")
İstanbul'un 5 günlük hava durumu tahmini
Bütün bu örneklerden sonra kafanızda söyle bir düsünce uyanmıs olabilir:
Görünüse göre üç tırnak isaretiyle her türlü karakter dizisini hatasız bir sekilde
ekrana çıktı olarak verebiliyoruz. O zaman ben en iyisi bütün karakter dizileri için
üç tırnak isaretini kullanayım!
Elbette, eger isterseniz pek çok karakter dizisi için üç tırnak isaretini kullanabilirsiniz.
Ancak Python’da karakter dizileri tanımlanırken genellikle tek tırnak veya çift tırnak isaretleri
kullanılır. Üç tırnak isaretlerinin asıl kullanım yeri ise farklıdır. Peki nedir bu üç tırnak
isaretlerinin asıl kullanım yeri?
Üç tırnak isaretlerini her türlü karakter dizisiyle birlikte kullanabiliyor olsak da, bu tırnak
tipi çogunlukla sadece birden fazla satıra yayılmıs karakter dizilerini tanımlamada kullanılır.
Örnegin söyle bir ekran çıktısı vermek istediginizi düsünün:
[H]=========HARMAN========[-][o][x]
| |
| Programa Hoşgeldiniz! |
| Sürüm 0.8 |
| Devam etmek için herhangi |
| bir düğmeye basın. |
| |
|=================================|
6.2. Nasıl Kullanılır? 53
Python 3 için Türkçe Kılavuz, Sürüm 3
Böyle bir çıktı verebilmek için eger tek veya çift tırnak kullanmaya kalkısırsanız epey eziyet
çekersiniz. Bu tür bir çıktı vermenin en kolay yolu üç tırnakları kullanmaktır:
>>> print("""
... [H]=========HARMAN========[-][o][x]
... | |
... | Programa Hoşgeldiniz! |
... | Sürüm 0.8 |
... | Devam etmek için herhangi |
... | bir düğmeye basın. |
... | |
... |=================================|
... """)
Burada bazı seyler dikkatinizi çekmis olmalı. Gördügünüz gibi, üç tırnaklı yapı öteki tırnak
tiplerine göre biraz farklı davranıyor. Simdi su örnege bakın:
>>> print("""Game Over!
...
Buraya çok dikkatli bakın. Karakter dizisine üç tırnakla basladıktan sonra, kapanıs tırnagını
koymadan Enter tusuna bastıgımızda >>> isareti ... isaretine dönüstü. Python bu sekilde
bize, ‘yazmaya devam et!’ demis oluyor. Biz de buna uyarak yazmaya devam edelim:
>>> print("""Game Over!
... Insert Coin!""")
Game Over!
Insert Coin!
Kapanıs tırnagı koyulmadan Enter tusuna basıldıgında >>> isaretinin ... isaretine dönüsmesi
üç tırnaga özgü bir durumdur. Eger aynı seyi tek veya çift tırnaklarla yapmaya çalısırsanız
programınız hata verir:
>>> print("Game Over!
File "<stdin>", line 1
print("Game Over!
^
SyntaxError: EOL while scanning string literal
...veya:
>>> print('Game Over!
File "<stdin>", line 1
print("Game Over!
^
SyntaxError: EOL while scanning string literal
Üç tırnak isaretlerinin tırnak kapanmadan Enter tusuna basıldıgında hata vermeme özelligi
sayesinde, bu tırnak tipi özellikle birden fazla satıra yayılmıs karakter dizilerinin gösterilmesi
için birebirdir.
Gelin isterseniz üç tırnak kullanımına iliskin bir örnek daha verelim:
>>> print("""Python programlama dili Guido Van Rossum
... adlı Hollandalı bir programcı tarafından 90’lı
54 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
... yılların başında geliştirilmeye başlanmıştır. Çoğu
... insan, isminin "Python" olmasına bakarak, bu programlama
... dilinin, adını piton yılanından aldığını düşünür.
... Ancak zannedildiğinin aksine bu programlama dilinin
... adı piton yılanından gelmez.""")
Python programlama dili Guido Van Rossum
adlı Hollandalı bir programcı tarafından 90'lı
yılların başında geliştirilmeye başlanmıştır. Çoğu
insan, isminin "Python" olmasına bakarak, bu programlama
dilinin, adını piton yılanından aldığını düşünür.
Ancak zannedildiğinin aksine bu programlama dilinin
dı piton yılanından gelmez.
Elbette eger istersek bu metni önce bir degiskene atamayı da tercih edebiliriz:
>>> python_hakkinda = """Python programlama dili Guido Van Rossum
... adlı Hollandalı bir programcı tarafından 90’lı
... yılların başında geliştirilmeye başlanmıştır. Çoğu
... insan, isminin "Python" olmasına bakarak, bu programlama
... dilinin, adını piton yılanından aldığını düşünür.
... Ancak zannedildiğinin aksine bu programlama dilinin
... adı piton yılanından gelmez."""
>>> print(python_hakkinda)
Python programlama dili Guido Van Rossum
adlı Hollandalı bir programcı tarafından 90'lı
yılların başında geliştirilmeye başlanmıştır. Çoğu
insan, isminin "Python" olmasına bakarak, bu programlama
dilinin, adını piton yılanından aldığını düşünür.
Ancak zannedildiğinin aksine bu programlama dilinin
dı piton yılanından gelmez.
Siz yukarıdaki çıktıyı tek veya çift tırnak kullanarak nasıl ekrana yazdırabileceginizi
düsünedurun, biz önemli bir konuya geçis yapalım!
Bir Fonksiyon Olarak print()
print() ifadesinin bir fonksiyon oldugunu söylemistik hatırlarsanız. Dedigimiz gibi,
fonksiyonlarla ilgili ayrıntılı açıklamaları ilerleyen derslerde verecegiz. Ancak simdi dilerseniz
bundan sonra anlatacaklarımızı daha iyi kavrayabilmemiz için, fonksiyonlar hakkında
bilmemiz gereken bazı temel seyleri ögrenmeye çalısalım.
Gördügünüz gibi, print() fonksiyonunu söyle kullanıyoruz:
>>> print("Aramak istediğiniz kelimeyi yazın: ")
Burada print() bir fonksiyon, “Aramak istediginiz kelimeyi yazın:” adlı karakter dizisi ise bu
fonksiyonun parametresidir. Daha önce len() adlı baska bir fonksiyon daha ögrenmistik
hatırlarsanız. Onu da söyle kullanıyorduk:
>>> len("elma")
Burada da len() bir fonksiyon, “elma” adlı karakter dizisi ise bu fonksiyonun parametresidir.
Aslında biçim olarak print() ve len() fonksiyonlarının birbirinden hiçbir farkı olmadıgını
6.3. Bir Fonksiyon Olarak print() 55
Python 3 için Türkçe Kılavuz, Sürüm 3
görüyorsunuz.
Daha önce söyledigimiz ve bu örneklerden de anladıgımız gibi, bir fonksiyonun parantezleri
içinde belirtilen ögelere parametre adı veriliyor. Mesela asagıdaki örnekte print()
fonksiyonunu tek bir parametre ile kullanıyoruz:
>>> print('En az 8 haneli bir parola belirleyin.')
print() fonksiyonu, tıpkı pow() fonksiyonu gibi, birden fazla parametre alabilir:
>>> print('Fırat', 'Özgül')
Fırat Özgül
Bu örnekte bizim için çıkarılacak çok dersler var. Bir defa burada print() fonksiyonunu iki
farklı parametre ile birlikte kullandık. Bunlardan ilki Fırat adlı bir karakter dizisi, ikincisi ise
Özgül adlı baska bir karakter dizisi. Python’ın bu iki karakter dizisini nasıl birlestirdigine dikkat
edin. print() fonksiyonu bu iki karakter dizisini çıktı olarak verirken aralarına da birer bosluk
yerlestirdi. Ayrıca, geçen derste de vurguladıgımız gibi, parametrelerin birbirinden virgül ile
ayrıldıgını da gözden kaçırmıyoruz.
Gelin bununla ilgili bir iki örnek daha verelim elimizin alısması için:
>>> print("Python", "Programlama", "Dili")
Python Programlama Dili
>>> print('Fırat', 'Özgül', 'Adana', 1980)
Fırat Özgül Adana 1980
Bu arada dikkatinizi önemli bir noktaya çekmek istiyorum. Yukarıdaki örneklerde bazen tek
tırnak, bazen de çift tırnak kullandık. Daha önce de söyledigimiz gibi, hangi tırnak tipini
kullandıgımız önemli degildir. Python hangi tırnak tipini kullandıgımızdan ziyade, tırnak
kullanımında tutarlı olup olmadıgımızla ilgilenir. Yani Python için önemli olan, karakter
dizisini hangi tırnakla baslatmıssak, o tırnakla bitirmemizdir. Yani su tip kullanımlar geçerli
degildir:
>>> print("karakter dizisi')
>>> print('karakter dizisi")
Karakter dizisini tanımlamaya baslarken kullandıgımız tırnak tipi ile karakter dizisini
tanımlamayı bitirirken kullandıgımız tırnak tipi birbirinden farklı oldugu için bu iki kullanım
da hata verecektir.
print() Fonksiyonunun Parametreleri
Simdiye kadar verdigimiz örneklerde belki çok da belli olmuyordur, ama aslında print()
fonksiyonu son derece güçlü bir araçtır. Iste simdi biz bu fonksiyonun gücünü gözler
önüne seren özelliklerini incelemeye baslayacagız. Bu bölümü dikkatle takip etmeniz, ilerde
yapacagımız çalısmaları daha rahat anlayabilmeniz açısından büyük önem tasır.
56 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
sep
print() fonksiyonu ile ilgili olarak yukarıda verdigimiz örnekleri inceledigimizde, bu
fonksiyonun kendine özgü bir davranıs sekli oldugunu görüyoruz. Mesela bir önceki bölümde
verdigimiz su örnege bakalım:
>>> print('Fırat', 'Özgül')
Fırat Özgül
Burada print() fonksiyonunu iki farklı parametre ile birlikte kullandık. Bu fonksiyon,
kendisine verdigimiz bu parametreleri belli bir düzene göre birbiriyle birlestirdi. Bu düzen
geregince print(), kendisine verilen parametreleri birlestirirken, parametreler arasına bir
bosluk yerlestiriyor. Bunu daha net görmek için söyle bir örnek daha verelim:
>>> print("Python", "PHP", "C++", "C", "Erlang")
Python PHP C++ C Erlang
Gördügünüz gibi, print() fonksiyonu gerçekten de, kendisine verilen parametreleri
birlestirirken, parametrelerin her biri arasına bir bosluk yerlestiriyor. Halbuki bu boslugu
biz talep etmedik! Python bize bu boslugu esantiyon olarak verdi. Çogu durumda istedigimiz
sey bu olacaktır, ama bazı durumlarda bu boslugu istemeyebiliriz. Örnegin:
>>> print("http://", "www.", "istihza.", "com")
http:// www. istihza. com
Ya da bosluk karakteri yerine daha farklı bir karakter kullanmak istiyor da olabiliriz. Peki böyle
bir durumda ne yapmamız gerekir?
Iste bu noktada bazı özel araçlardan yararlanarak print() fonksiyonunun öntanımlı davranıs
kalıpları üzerinde degisiklikler yapabiliriz.
Peki nedir print() fonksiyonunu özellestirmemizi saglayacak bu araçlar?
Hatırlarsanız, Python’da fonksiyonların parantezleri içindeki degerlere parametre adı
verildigini söylemistik. Mesela print() fonksiyonunu bir ya da daha fazla parametre ile
birlikte kullanabilecegimizi biliyoruz:
>>> print("Mehmet", "Öz", "İstanbul", "Çamlıca", 156, "/", 45)
Mehmet Öz İstanbul Çamlıca 156 / 45
print() fonksiyonu içinde istedigimiz sayıda karakter dizisi ve/veya sayı degerli parametre
kullanabiliriz.
Fonksiyonların bir de daha özel görünümlü parametreleri vardır. Mesela print()
fonksiyonunun sep adlı özel bir parametresi bulunur. Bu parametre print() fonksiyonunda
görünmese bile her zaman oradadır. Yani diyelim ki söyle bir kod yazdık:
>>> print("http://", "www.", "google.", "com")
Burada herhangi bir sep parametresi görmüyoruz. Ancak Python yukarıdaki kodu aslında
söyle algılar:
6.4. print() Fonksiyonunun Parametreleri 57
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> print("http://", "www.", "google.", "com", sep=" ")
sep ifadesi, Ingilizcede separator (ayırıcı, ayraç) kelimesinin kısaltmasıdır. Dolayısıyla
print() fonksiyonundaki bu sep parametresi, ekrana basılacak ögeler arasına hangi
karakterin yerlestirilecegini gösterir. Bu parametrenin öntanımlı degeri bir adet bosluk
karakteridir (” “ ). Yani siz bu özel parametrenin degerini baska bir seyle degistirmezseniz,
Python bu parametrenin degerini bir adet bosluk karakteri olarak alacak ve ekrana basılacak
ögeleri birbirinden birer boslukla ayıracaktır. Ancak eger biz istersek bu sep parametresinin
degerini degistirebiliriz. Böylece Python, karakter dizilerini birlestirirken araya bosluk degil,
bizim istedigimiz baska bir karakteri yerlestirebilir. Gelin simdi bu parametrenin degerini
nasıl degistirecegimizi görelim:
>>> print("http://", "www.", "istihza.", "com", sep="")
http://www.istihza.com
Gördügünüz gibi, karakter dizilerini basarıyla birlestirip, geçerli bir internet adresi elde ettik.
Burada yaptıgımız sey aslında çok basit. Sadece sep parametresinin ‘bir adet bosluk karakteri’
olan öntanımlı degerini silip, yerine ‘bos bir karakter dizisi’ degerini yazdık. Bu iki kavramın
birbirinden farklı oldugunu söyledigimizi hatırlıyorsunuz, degil mi?
Gelin bir örnek daha yapalım:
>>> print("T", "C", sep=".")
T.C
Burada Python’a söyle bir emir vermis olduk:
“T” ve “C” karakter dizilerini birbiriyle birlestir! Bunu yaparken de bu karakter
dizilerinin arasına nokta isareti yerlestir!
sep parametresinin öteki parametrelerden farkı her zaman ismiyle birlikte kullanılmasıdır.
Zaten teknik olarak da bu tür parametrelere ‘isimli parametreler’ adı verilir. Örnegin:
>>> print("Adana", "Mersin", sep="-")
Adana-Mersin
Eger burada sep parametresinin ismini belirtmeden, dogrudan parametrenin degerini
yazarsak, bu degerin öteki parametrelerden hiçbir farkı kalmayacaktır:
>>> print("Adana", "Mersin", "-")
Adana Mersin -
Gelin isterseniz bu parametreyle ilgili bir örnek daha yapalım:
‘Bir mumdur iki mumdur...’ diye baslayan türküyü biliyorsunuzdur. Simdi bu türküyü
Python’la nasıl yazabilecegimizi görelim!
>>> print("bir", "iki", "üç", "dört", "on dört", sep="mumdur")
birmumdurikimumdurüçmumdurdörtmumduron dört
Burada bir terslik oldugu açık! Karakter dizileri birbirlerine sıkısık düzende birlestirildi.
Bunların arasında birer bosluk olsa tabii daha iyi olurdu. Ancak biliyorsunuz sep
58 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
parametresinin öntanımlı degerini silip, yerine “mumdur” degerini yerlestirdigimiz için,
Python’ın otomatik olarak yerlestirdigi bosluk karakteri kayboldu. Ama eger istersek o bosluk
karakterlerini kendimiz de ayarlayabiliriz:
>>> print("bir", "iki", "üç", "dört", "on dört", sep=" mumdur ")
bir mumdur iki mumdur üç mumdur dört mumdur on dört
Gördügünüz gibi, sep parametresine verdigimiz “mumdur” degerinin sagında ve solunda
birer bosluk bırakarak sorunumuzu çözebildik. Bu sorunu çözmenin baska bir yolu daha
var. Hatırlarsanız etkilesimli kabukta ilk örneklerimizi verirken karakter dizilerini birlestirmek
için + isaretinden de yararlanabilecegimizi söylemistik. Dolayısıyla sep parametresini söyle
de yazabiliriz:
>>> print("bir", "iki", "üç", "dört", "on dört", sep=" " + "mumdur" + " ")
Burada da, “mumdur” adlı karakter dizisinin basında ve sonunda birer bosluk bırakmak
yerine, gerekli boslukları + isareti yardımıyla bu karakter dizisine birlestirdik. Hatta istersek +
islecini kullanmak zorunda olmadıgımızı dahi biliyorsunuz:
>>> print("bir", "iki", "üç", "dört", "on dört", sep=" " "mumdur" " ")
Ama gördügünüz gibi bir problemimiz daha var. Türkünün sözleri su sekilde olmalıydı:
bir mumdur iki mumdur üç mumdur dört mumdur on dört mumdur
Ama sondaki ‘mumdur’ kelimesi yukarıdaki çıktıda yok. Normal olan da bu aslında. sep
parametresi, karakter dizilerinin arasına bir deger yerlestirir. Karakter dizilerinin son tarafıyla
ilgilenmez. Bu is için print() fonksiyonu baska bir parametreye sahiptir.
Bu arada, yukarıdaki örneklerde hep karakter dizilerini kullanmıs olmamız sizi yanıltmasın.
sep parametresi yalnızca karakter dizilerinin degil sayıların arasına da istediginiz bir degerin
yerlestirilmesini saglayabilir. Mesela:
>>> print(1, 2, 3, 4, 5, sep="-")
1-2-3-4-5
Ancak sep parametresine deger olarak yalnızca karakter dizilerini ve None adlı özel bir
sözcügü verebiliriz. (None sözcügünden ileride söz edecegiz):
>>> print(1, 2, 3, 4, 5, sep=0)
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: sep must be None or a string, not int
Gördügünüz gibi, sep parametresine bir sayı olan 0 degerini veremiyoruz.
Peki bu parametreye None degeri verirsek ne olur? Bu parametreye None degeri
verildiginde, print() fonksiyonu bu parametre için öntanımlı degeri (yani bir adet bosluk)
kullanır:
>>> print('a', 'b', sep=None)
a b
6.4. print() Fonksiyonunun Parametreleri 59
Python 3 için Türkçe Kılavuz, Sürüm 3
Eger amacınız parametreleri birbirine bitistirmekse, yani sep parametresinin öntanımlı degeri
olan bosluk karakterini ortadan kaldırmaksa, sep parametresine bos bir karakter dizisi
vermeniz gerektigini biliyorsunuz:
>>> print('a', 'b', sep='')
ab
print() fonksiyonunun sep parametresini bütün ayrıntılarıyla inceledigimize göre, bu
fonksiyonun bir baska özel parametresinden söz edebiliriz.
end
Bir önceki bölümde söyle bir laf etmistik:
print() fonksiyonun sep adlı özel bir parametresi bulunur. Bu parametre
print() fonksiyonunda görünmese bile her zaman oradadır.
Aynı bu sekilde, print() fonksiyonunun end adlı özel bir parametresi daha bulunur. Tıpkı
sep parametresi gibi, end parametresi de print() fonksiyonunda görünmese bile her zaman
oradadır.
Bildiginiz gibi, sep parametresi print() fonksiyonuna verilen parametreler birlestirilirken
araya hangi karakterin girecegini belirliyordu. end parametresi ise bu parametrelerin sonuna
neyin gelecegini belirler.
print() fonksiyonu öntanımlı olarak, parametrelerin sonuna ‘satır bası karakteri’ ekler. Peki
bu satır bası karakteri (veya ‘yeni satır karakteri’) denen sey de ne oluyor?
Dilerseniz bunu bir örnek üzerinde görelim.
Söyle bir kodumuz olsun:
>>> print("Pardus ve Ubuntu birer GNU/Linux dağıtımıdır.")
Bu kodu yazıp Enter tusuna bastıgımız anda print() fonksiyonu iki farklı islem gerçeklestirir:
1. Öncelikle karakter dizisini ekrana yazdırır.
2. Ardından bir alt satıra geçip bize >>> isaretini gösterir.
Iste bu ikinci islem, karakter dizisinin sonunda bir adet satır bası karakteri olmasından,
daha dogrusu print() fonksiyonunun, satır bası karakterini karakter dizisinin sonuna
eklemesinden kaynaklanır. Bu açıklama biraz kafa karıstırıcı gelmis olabilir. O halde biraz
daha açıklayalım. Su örnege bakın:
>>> print("Pardus\nUbuntu")
Pardus
Ubuntu
Burada “Pardus” ve “Ubuntu” karakter dizilerinin tam ortasında çok özel bir karakter dizisi
daha görüyorsunuz. Bu karakter dizisi sudur: \n. Iste bu özel karakter dizisine satır bası
karakteri (newline) adı verilir. Bu karakterin görevi, karakter dizisini, bulundugu noktadan
bölüp, karakter dizisinin geri kalanını bir alt satıra geçirmektir. Zaten çıktıda da bu islevi
yerine getirdigini görüyorsunuz. Karakter dizisi “Pardus” kısmından sonra ikiye bölünüyor ve
bu karakter dizisinin geri kalan kısmı olan “Ubuntu” karakter dizisi bir alt satıra yazdırılıyor.
Bunu daha iyi anlamak için bir örnek daha verelim:
60 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> print("birinci satır\nikinci satır\nüçüncü satır")
birinci satır
ikinci satır
üçüncü satır
Peki size bir soru sorayım: Acaba yukarıdaki kodları daha verimli bir sekilde nasıl yazabiliriz?
Evet, dogru tahmin ettiniz... Tabii ki sep parametresini kullanarak:
>>> print("birinci satır", "ikinci satır", "üçüncü satır", sep="\n")
birinci satır
ikinci satır
üçüncü satır
Burada yaptıgımız sey çok basit. sep parametresinin degerini \n, yani yeni satır karakteri
(veya satır bası karakteri) olarak degistirdik. Böylece karakter dizileri arasına birer \n karakteri
yerlestirerek her bir karakter dizisinin farklı satıra yazdırılmasını sagladık.
Iste end parametresinin öntanımlı degeri de bu \n karakteridir ve bu parametre print()
fonksiyonunda görünmese bile her zaman oradadır.
Yani diyelim ki söyle bir kod yazdık:
>>> print("Bugün günlerden Salı")
Burada herhangi bir end parametresi görmüyoruz. Ancak Python yukarıdaki kodu aslında
söyle algılar:
>>> print("Bugün günlerden Salı", end="\n")
Biraz önce de dedigimiz gibi, bu kodu yazıp Enter tusuna bastıgımız anda print() fonksiyonu
iki farklı islem gerçeklestirir:
1. Öncelikle karakter dizisini ekrana yazdırır.
2. Ardından bir alt satıra geçip bize >>> isaretini gösterir.
Bunun ne demek oldugunu anlamak için end parametresinin degerini degistirmemiz yeterli
olacaktır:
>>> print("Bugün günlerden Salı", end=".")
Bugün günlerden Salı.>>>
Gördügünüz gibi, end parametresinin öntanımlı degeri olan \n karakterini silip yerine .
(nokta) isareti koydugumuz için, komutu yazıp Enter tusuna bastıgımızda print() fonksiyonu
satır basına geçmedi. Yeni satıra geçebilmek için Enter tusuna kendimiz basmalıyız. Elbette,
eger yukarıdaki kodları söyle yazarsanız, print() fonksiyonu hem karakter dizisinin sonuna
nokta ekleyecek, hem de satır basına geçecektir:
>>> print("Bugün günlerden Salı", end=".\n")
Bugün günlerden Salı.
Simdi bu ögrendiklerimizi türkümüze uygulayalım:
6.4. print() Fonksiyonunun Parametreleri 61
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> print("bir", "iki", "üç", "dört", "on dört",
... sep=" mumdur ", end=" mumdur\n")
Not: Burada kodlarımızın saga dogru çirkin bir sekilde uzamasını engellemek için “on dört”
karakter dizisini yazıp virgülü koyduktan sonra Enter tusuna basarak bir alt satıra geçtik.
Bir alt satıra geçtigimizde >>> isaretinin ... isaretine dönüstügüne dikkat edin. Python’da
dogru kod yazmak kadar, yazdıgımız kodların düzgün görünmesi de önemlidir. O yüzden
yazdıgımız her bir kod satırının mümkün oldugunca 79 karakteri geçmemesini saglamalıyız.
Eger yazdıgınız bir satır 79 karakteri asıyorsa, asan kısmı yukarıda gösterdigimiz sekilde alt
satıra alabilirsiniz.
end parametresi de, tıpkı sep parametresi gibi, her zaman ismiyle birlikte kullanılması
gereken bir parametredir. Yani eger end parametresinin ismini belirtmeden sadece degerini
kullanmaya çalısırsak Python ne yapmaya çalıstıgımızı anlayamaz.
Yine tıpkı sep parametresi gibi, end parametresinin degeri de sadece bir karakter dizisi veya
None olabilir:
>>> print(1, 2, 3, 4, 5, end=0)
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: end must be None or a string, not int
Gördügünüz gibi, end parametresine bir sayı olan 0 degerini veremiyoruz.
Eger bu parametreye None degeri verirsek, tıpkı sep parametresinde oldugu gibi, print()
fonksiyonu bu parametre için öntanımlı degeri (yani satır bası karakteri) kullanır:
>>> print('a', 'b', end=None)
a b
Eger amacınız yeni satıra geçilmesini engellemekse, yani end parametresinin öntanımlı
degeri olan \n kaçıs dizisini ortadan kaldırmaksa, end parametresine bos bir karakter dizisi
vermelisiniz:
>>> print('a', 'b', end='')
a b>>>
1le
Not: Burada henüz ögrenmedigimiz bazı seyler göreceksiniz. Hiç endise etmeyin. Bunları
ilerde bütün ayrıntılarıyla ögrenecegiz. Simdilik konu hakkında biraz olsun 1kir sahibi
olmanızı saglayabilirsek kendimizi basarılı sayacagız.
print() fonksiyonunun sep ve end dısında üçüncü bir özel parametresi daha bulunur. Bu
parametrenin adı 1le ‘dır. Görevi ise, print() fonksiyonuna verilen karakter dizisi ve/veya
sayıların, yani parametrelerin nereye yazılacagını belirtmektir.
62 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
Bu parametrenin öntanımlı degeri sys.stdout ‘tur. Peki bu ne anlama geliyor? sys.stdout,
‘standart çıktı konumu’ anlamına gelir. Peki ‘standart çıktı konumu’ ne demek?
Standart çıktı konumu; bir programın, ürettigi çıktıları verdigi yerdir. Aslında bu kavramın ne
demek oldugu adından da anlasılıyor:
standart çıktı konumu = çıktıların standart olarak verildigi konum.
Mesela Python öntanımlı olarak, ürettigi çıktıları ekrana verir. Eger o anda etkilesimli kabukta
çalısıyorsanız, Python ürettigi çıktıları etkilesimli kabuk üzerinde gösterir. Eger yazdıgınız
bir programı komut satırında çalıstırıyorsanız, üretilen çıktılar komut satırında görünür.
Dolayısıyla Python’ın standart çıktı konumu etkilesimli kabuk veya komut satırıdır. Yani
print() fonksiyonu yardımıyla bastıgınız çıktılar etkilesimli kabukta ya da komut satırında
görünecektir.
Simdi bu konuyu daha iyi anlayabilmek için birkaç örnek yapalım.
Normal sartlar altında print() fonksiyonunun çıktısını etkilesimli kabukta görürüz:
>>> print("Ben Python, Monty Python!")
Ben Python, Monty Python!
Ama eger istersek print() fonksiyonunun, çıktılarını ekrana degil, bir dosyaya yazdırmasını
da saglayabiliriz. Mesela biz simdi print() fonksiyonunun deneme.txt adlı bir dosyaya çıktı
vermesini saglayalım.
Bunun için sırasıyla su kodları yazalım:
>>> dosya = open("deneme.txt", "w")
>>> print("Ben Python, Monty Python!", file=dosya)
>>> dosya.close()
Herhangi bir çıktı almadınız, degil mi? Evet. Çünkü yazdıgımız bu kodlar sayesinde print()
fonksiyonu, çıktılarını deneme.txt adlı bir dosyaya yazdırdı.
Gelin isterseniz yukarıdaki kodları satır satır inceleyelim:
1. Öncelikle deneme.txt adlı bir dosya olusturduk ve bu dosyayı dosya adlı bir degiskene
atadık. Burada kullandıgımız open() fonksiyonuna çok takılmayın. Bunu birkaç bölüm sonra
inceleyecegiz. Biz simdilik bu sekilde dosya olusturuldugunu bilelim yeter. Bu arada open
fonksiyonunun da biçim olarak type(), len(), pow() ve print() fonksiyonlarına ne kadar
benzedigine dikkat edin. Gördügünüz gibi open() fonksiyonu da tıpkı type(), len(), pow()
ve print() fonksiyonları gibi birtakım parametreler alıyor. Bu fonksiyonun ilk parametresi
“deneme.txt” adlı bir karakter dizisi. Iste bu karakter dizisi bizim olusturmak istedigimiz
dosyanın adını gösteriyor. Ikinci parametre ise “w” adlı baska bir karakter dizisi. Bu da
deneme.txt dosyasının yazma kipinde (modunda) açılacagını gösteriyor. Ama dedigim gibi,
siz simdilik bu ayrıntılara fazla takılmayın. Ilerleyen derslerde, bu konuları adınızı bilir gibi
bileceginizden emin olabilirsiniz.
2. Olusturdugumuz bu deneme.txt adlı dosya, o anda bulundugunuz dizin içinde olusacaktır.
Bu dizinin hangisi oldugunu ögrenmek için su komutları verebilirsiniz:
>>> import os
>>> os.getcwd()
Bu komutun çıktısında hangi dizinin adı görünüyorsa, deneme.txt dosyası da o dizinin
içindedir. Mesela bendeki çıktı /home/istihza/Desktop. Demek ki olusturdugum deneme.txt
6.4. print() Fonksiyonunun Parametreleri 63
Python 3 için Türkçe Kılavuz, Sürüm 3
adlı dosya masaüstündeymis. Ben bu komutları Ubuntu üzerinde verdim. Eger Windows
üzerinde verseydim suna benzer bir çıktı alacaktım: C:\Users\istihza\Desktop
3. Ardından da normal bir sekilde print() fonksiyonumuzu çalıstırdık. Ama gördügünüz gibi
print() fonksiyonu bize herhangi bir çıktı vermedi. Çünkü, daha önce de söyledigimiz gibi,
print() fonksiyonunu biz ekrana degil, dosyaya çıktı verecek sekilde ayarladık. Bu islemi, 1le
adlı bir parametreye, biraz önce tanımladıgımız dosya degiskenini yazarak yaptık.
4. Son komut yardımıyla da, yaptıgımız degisikliklerin dosyada görünebilmesi için ilk basta
açtıgımız dosyayı kapatıyoruz.
Simdi deneme.txt adlı dosyayı açın. Biraz önce print() fonksiyonuyla yazdırdıgımız “Ben
Python, Monty Python!” karakter dizisinin dosyaya islenmis oldugunu göreceksiniz.
Böylece print() fonksiyonunun standart çıktı konumunu degistirmis olduk. Yani print()
fonksiyonunun 1le adlı parametresine farklı bir deger vererek, print() fonksiyonunun
etkilesimli kabuga degil dosyaya yazmasını sagladık.
Tıpkı sep ve end parametreleri gibi, 1le parametresi de, siz görmeseniz bile her zaman
print() fonksiyonunun içinde vardır. Yani diyelim ki söyle bir komut verdik:
>>> print("Tahir olmak da ayıp değil", "Zühre olmak da")
Python bu komutu söyle algılar:
>>> print("Tahir olmak da ayıp değil", "Zühre olmak da",
... sep=" ", end="\n", file=sys.stdout)
Yani kendisine parametre olarak verilen degerleri ekrana yazdırırken sırasıyla su islemleri
gerçeklestirir:
1. Parametrelerin arasına birer bosluk koyar (sep=" "),
2. Ekrana yazdırma islemi bittikten sonra parametrelerin sonuna satır bası karakteri ekler
(end="\n")
3. Bu çıktıyı standart çıktı konumuna gönderir (file=sys.stdout).
Iste biz burada 1le parametresinin degeri olan standart çıktı konumuna baska bir deger
vererek bu konumu degistiriyoruz.
Gelin isterseniz bununla ilgili bir örnek daha yapalım. Mesela kisisel bilgilerimizi bir dosyaya
kaydedelim. Öncelikle bilgileri kaydedecegimiz dosyayı olusturalım:
>>> f = open("kişisel_bilgiler.txt", "w")
Bu kodlarla, kisisel_bilgiler.txt adını tasıyan bir dosyayı yazma kipinde (w) açmıs ve bu dosyayı
f adlı bir degiskene atamıs olduk. Simdi bilgileri yazmaya baslayabiliriz:
>>> print("Fırat Özgül", file=f)
>>> print("Adana", file=f)
>>> print("Ubuntu", file=f)
Isimiz bittiginde dosyayı kapatmayı unutmuyoruz. Böylece bütün bilgiler dosyaya yazılmıs
oluyor:
>>> f.close()
Olusturdugumuz kisisel_bilgiler.txt adlı dosyayı açtıgımızda, print() fonksiyonuna verdigimiz
parametrelerin dosyaya yazdırıldıgını görüyoruz.
64 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
En basta da söyledigim gibi, bu bölümde henüz ögrenmedigimiz bazı seylerle karsılastık. Eger
yukarıda verilen örnekleri anlamakta zorlandıysanız hiç endise etmenize gerek yok. Birkaç
bölüm sonra burada anlattıgımız seyler size çocuk oyuncagı gibi gelecek...
2ush
Simdiye kadar print() fonksiyonunun sep, end ve 1le adlı özel birtakım parametreleri
oldugunu ögrendik. print() fonksiyonunun bunların dısında baska bir özel parametresi daha
bulunur. Bu parametrenin adı 2ush. Iste simdi biz print() fonksiyonunun bu 2ush adlı
parametresinden söz edecegiz.
Bildiginiz gibi, print() gibi bir komut verdigimizde Python, yazdırmak istedigimiz bilgiyi
standart çıktı konumuna gönderir. Ancak Python’da bazı islemler standart çıktı konumuna
gönderilmeden önce bir süre tamponda bekletilir ve daha sonra bekleyen bu islemler topluca
standart çıktı konumuna gönderilir. Peki ilk basta çok karmasıkmıs gibi görünen bu ifade ne
anlama geliyor?
Aslında siz bu olguya hiç yabancı degilsiniz. 1le parametresini anlatırken verdigimiz su örnegi
tekrar ele alalım:
>>> f = open("kişisel_bilgiler.txt", "w")
Bu komutla kisisel_bilgiler.txt adlı bir dosyayı yazma kipinde açtık. Simdi bu dosyaya bazı
bilgiler ekleyelim:
>>> print("Fırat Özgül", file=f)
Bu komutla kisisel_bilgiler.txt adlı dosyaya ‘Fırat Özgül’ diye bir satır eklemis olduk.
Simdi bilgisayarınızda olusan bu kisisel_bilgiler.txt dosyasını açın. Gördügünüz gibi dosyada
hiçbir bilgi yok. Dosya su anda bos görünüyor. Halbuki biz biraz önce bu dosyaya ‘Fırat Özgül’
diye bir satır eklemistik, degil mi?
Python bizim bu dosyaya eklemek istedigimiz satırı tampona kaydetti. Dosyaya yazma
islemleri sona erdiginde ise Python, tamponda bekleyen bütün bilgileri standart çıktı
konumuna (yani bizim durumumuzda f adlı degiskenin tuttugu kisisel_bilgiler.txt adlı
dosyaya) bosaltacak.
Dosyaya baska bilgiler de yazalım:
>>> print("Adana", file=f)
>>> print("Ubuntu", file=f)
Dosyaya yazacagımız seyler bu kadar. Artık yazma isleminin sona erdigini Python’a bildirmek
için su komutu veriyoruz:
>>> f.close()
Böylece dosyamızı kapatmıs olduk. Simdi kisisel_bilgiler.txt adlı dosyaya çift tıklayarak
dosyayı tekrar açın. Orada ‘Fırat Özgül’, ‘Adana’ ve ‘Ubuntu’ satırlarını göreceksiniz.
Gördügünüz gibi, gerçekten de Python dosyaya yazdırmak istedigimiz bütün verileri önce
tamponda bekletti, daha sonra dosya kapatılınca tamponda bekleyen bütün verileri dosyaya
bosalttı. Iste 2ush parametresi ile, bahsettigimiz bu bosaltma islemini kontrol edebilirsiniz.
Simdi dikkatlice inceleyin:
6.4. print() Fonksiyonunun Parametreleri 65
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> f = open("kişisel_bilgiler.txt", "w")
Dosyamızı olusturduk. Simdi bu dosyaya bazı bilgiler ekleyelim:
>>> print("Merhaba Dünya!", file=f, flush=True)
Gördügünüz gibi, burada 2ush adlı yeni bir parametre kullandık. Bu parametreye verdigimiz
deger True. Simdi dosyaya çift tıklayarak dosyayı açın. Gördügünüz gibi, henüz dosyayı
kapatmadıgımız halde bilgiler dosyaya yazıldı. Bu durum, tahmin edebileceginiz gibi, 2ush
parametresine True degeri vermemiz sayesindedir. Bu parametre iki deger alabilir: True ve
False. Bu parametrenin öntanımlı degeri False ‘tur. Yani eger biz bu parametreye herhangi
bir deger belirtmezsek Python bu parametrenin degerini False olarak kabul edecek ve
bilgilerin dosyaya yazılması için dosyanın kapatılmasını bekleyecektir. Ancak bu parametreye
True degerini verdigimizde ise veriler tamponda bekletilmeksizin standart çıktı konumuna
gönderilecektir.
Yazdıgınız bir programda, yapmak istediginiz isin niteligine göre, bir dosyaya yazmak
istediginiz bilgilerin bir süre tamponda bekletilmesini veya hiç bekletilmeden dogrudan
dosyaya yazılmasını isteyebilirsiniz. Ihtiyacınıza baglı olarak da 2ush parametresinin degerini
True veya False olarak belirleyebilirsiniz.
Birkaç Pratik Bilgi
Buraya gelene kadar print() fonksiyonu ve bu fonksiyonun parametreleri hakkında epey
söz söyledik. Dilerseniz simdi de, programcılık maceranızda isinize yarayacak, islerinizi
kolaylastıracak bazı ipuçları verelim.
Yıldızlı Parametreler
Simdi size söyle bir soru sormama izin verin: Acaba asagıdaki gibi bir çıktıyı nasıl elde ederiz?
L.i.n.u.x
Aklınıza hemen söyle bir cevap gelmis olabilir:
>>> print("L", "i", "n", "u", "x", sep=".")
L.i.n.u.x
Yukarıdaki, gerçekten de dogru bir çözümdür. Ancak bu soruyu çözmenin çok daha basit bir
yolu var. Simdi dikkatle bakın:
>>> print(*"Linux", sep=".")
L.i.n.u.x
Konuyu açıklamaya geçmeden önce bir örnek daha verelim:
>>> print(*"Galatasaray")
G a l a t a s a r a y
Burada neler döndügünü az çok tahmin ettiginizi zannediyorum. Son örnekte de gördügünüz
gibi, “Galatasaray” karakter dizisinin basına ekledigimiz yıldız isareti; “Galatasaray” karakter
66 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
dizisinin her bir ögesini parçalarına ayırarak, bunları tek tek print() fonksiyonuna yolluyor.
Yani sanki print() fonksiyonunu söyle yazmısız gibi oluyor:
>>> print("G", "a", "l", "a", "t", "a", "s", "a", "r", "a", "y")
G a l a t a s a r a y
Dedigimiz gibi, bir fonksiyona parametre olarak verdigimiz bir karakter dizisinin basına
ekledigimiz yıldız isareti, bu karakter dizisini tek tek ögelerine ayırıp, bu ögeleri yine tek tek ve
sanki her bir öge ayrı bir parametreymis gibi o fonksiyona gönderdigi için dogal olarak yıldız
isaretini ancak, birden fazla parametre alabilen fonksiyonlara uygulayabiliriz.
Örnegin len() fonksiyonu sadece tek bir parametre alabilir:
>>> len("Galatasaray")
11
Bu fonksiyonu birden fazla parametre ile kullanamayız:
>>> len("Galatasaray", "Fenerbahçe", "Beşiktaş")
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: len() takes exactly one argument (3 given)
Hata mesajında da söylendigi gibi, len() fonksiyonu yalnızca tek bir parametre alabilirken,
biz 3 parametre vermeye çalısmısız...
Dolayısıyla yıldızlı parametreleri len() fonksiyonuna uygulayamayız:
>>> len(*"Galatasaray")
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: len() takes exactly one argument (11 given)
Bir parametrenin basına yıldız ekledigimizde, o parametreyi olusturan bütün ögeler tek tek
fonksiyona gönderildigi için, sanki len() fonksiyonuna 1 degil de, 11 ayrı parametre vermisiz
gibi bir sonuç ortaya çıkıyor.
Yıldızlı parametreleri bir fonksiyona uygulayabilmemiz için o fonksiyonun birden fazla
parametre alabilmesinin yanısıra, yapısının da yıldızlı parametre almaya uygun olması
gerekir. Mesela open(), type() ve biraz önce bahsettigimiz len() fonksiyonlarının yapısı
yıldızlı parametre almaya uygun degildir. Dolayısıyla yıldızlı parametreleri her fonksiyonla
birlikte kullanamayız, ama print() fonksiyonu yıldızlı parametreler için son derece uygun bir
fonksiyondur:
>>> print(*"Galatasaray")
G a l a t a s a r a y
>>> print(*"TBMM", sep=".")
T.B.M.M
>>> print(*"abcçdefgğh", sep="/")
6.5. Birkaç Pratik Bilgi 67
Python 3 için Türkçe Kılavuz, Sürüm 3
a/b/c/ç/d/e/f/g/ğ/h
Bu örneklerden de gördügünüz gibi, print() fonksiyonuna verdigimiz bir parametrenin
basına yıldız ekledigimizde, o parametre tek tek parçalarına ayrılıp print() fonksiyonuna
gönderildigi için, sonuç olarak sep parametresinin karakter dizisi ögelerine tek tek
uygulanmasını saglamıs oluyoruz.
Hatırlarsanız sep parametresinin öntanımlı degerinin bir adet bosluk karakteri oldugunu
söylemistik. Yani aslında Python yukarıdaki ilk komutu söyle görüyor:
>>> print(*"Galatasaray", sep=" ")
Dolayısıyla, yıldız isareti sayesinde “Galatasaray” adlı karakter dizisinin her bir ögesinin
arasına bir adet bosluk karakteri yerlestiriliyor. Bir sonraki “TBMM” karakter dizisinde ise, sep
parametresinin degerini nokta isareti olarak degistirdigimiz için “TBMM” karakter dizisinin
her bir ögesinin arasına bir adet nokta isareti yerlestiriliyor. Aynı sekilde “abcçdefggh”
karakter dizisinin her bir ögesini tek tek print() fonksiyonuna yollayarak, sep parametresine
verdigimiz / isareti yardımıyla her ögenin arasına bu / isaretini yerlestirebiliyoruz.
Yıldızlı parametrelerle ilgili tek kısıtlama, bunların sayılarla birlikte kullanılamayacak
olmasıdır:
>>> print(*2345)
Traceback (most recent call last):
File "<stdin>", line 1, in <module>
TypeError: print() argument after * must be a sequence, not int
Çünkü yıldızlı parametreler ancak ve ancak dizi özelligi tasıyan veri tipleriyle birlikte
kullanılabilir. Mesela karakter dizileri bu türden bir veri tipidir. Ilerde dizi özelligi tasıyan ve
bu sayede yıldızlı parametrelerle birlikte kullanılabilecek baska veri tiplerini de ögrenecegiz.
Yukarıda verdigimiz örnekler bize yıldızlı parametrelerin son derece kullanıslı araçlar
oldugunu gösteriyor. Ileride de bu parametrelerden bol bol yararlanacagız. Biz simdi bu
konuyu burada kapatıp baska bir seyden söz edelim.
sys.stdout’u Kalıcı Olarak Degistirmek
Önceki baslıklar altında verdigimiz örneklerden de gördügünüz gibi, print() fonksiyonunun
1le parametresi yardımıyla Python’ın standart çıktı konumunu geçici olarak degistirebiliyoruz.
Ama bazı durumlarda, yazdıgınız programlarda, o programın isleyisi boyunca standart dısı
bir çıktı konumu belirlemek isteyebilirsiniz. Yani standart çıktı konumunu geçici olarak
degil, kalıcı olarak degistirmeniz gerekebilir. Mesela yazdıgınız programda bütün çıktıları bir
dosyaya yazdırmayı tercih edebilirsiniz. Elbette bu islemi her defasında 1le parametresini,
çıktıları yazdırmak istediginiz dosyanın adı olarak belirleyerek yapabilirsiniz. Tıpkı su örnekte
oldugu gibi:
>>> f = open("dosya.txt", "w")
>>> print("Fırat Özgül", file=f)
>>> print("Adana", file=f)
>>> print("Ubuntu", file=f)
>>> f.close()
68 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
Gördügünüz gibi, her defasında 1le parametresine f degerini vererek isimizi hallettik. Ama
bunu yapmanın daha pratik bir yöntemi var. Dilerseniz yazdıgınız programın tüm isleyisi
boyunca çıktıları baska bir konuma yönlendirebilirsiniz. Bunun için hem simdiye kadar
ögrendigimiz, hem de henüz ögrenmedigimiz bazı bilgileri kullanacagız.
Ilk önce söyle bir kod yazalım:
>>> import sys
Bu kod yardımıyla sys adlı özel bir ‘modülü’ programımıza dahil etmis, yani içe aktarmıs olduk.
Peki ‘modül’ nedir, ‘içe aktarmak’ ne demek?
Aslında biz bu ‘modül’ ve ‘içe aktarma’ kavramlarına hiç de yabancı degiliz. Önceki derslerde,
pek üzerinde durmamıs da olsak, biz Python’daki birkaç modülle zaten tanısmıstık. Mesela
os adlı bir modül içindeki getcwd() adlı bir fonksiyonu kullanarak, o anda hangi dizinde
bulundugumuzu ögrenebilmistik:
>>> import os
>>> os.getcwd()
Aynı sekilde keyword adlı baska bir modül içindeki kwlist adlı degiskeni kullanarak, hangi
kelimelerin Python’da degisken adı olarak kullanılamayacagını da listeleyebilmistik:
>>> import keyword
>>> keyword.kwlist
Iste simdi de, os ve keyword modüllerine ek olarak sys adlı bir modülden söz ediyoruz.
Gelin isterseniz öteki modülleri simdilik bir kenara bırakıp, bu sys denen modüle dikkatimizi
verelim.
Dedigimiz gibi, sys modülü içinde pek çok önemli degisken ve fonksiyon bulunur. Ancak bir
modül içindeki degisken ve fonksiyonları kullanabilmek için o modülü öncelikle programımıza
dahil etmemiz, yani içe aktarmamız gerekiyor. Bunu import komutuyla yapıyoruz:
>>> import sys
Artık sys modülü içindeki bütün fonksiyon ve degiskenlere ulasabilecegiz.
sys modülü içinde bulunan pek çok degisken ve fonksiyondan biri de stdout adlı degiskendir.
Bu degiskenin degerine söyle ulasabilirsiniz:
>>> sys.stdout
Bu komut suna benzer bir çıktı verir:
<_io.TextIOWrapper name='<stdout>' mode='w' encoding='cp1254'>
Bu çıktıdaki name=’<stdout>’ kısmına dikkat edin. Bu ifadeye birazdan geri dönecegiz. Biz
simdi baska bir seyden söz edelim.
Hatırlarsanız etkilesimli kabugu nasıl kapatabilecegimizi anlatırken, etkilesimli kabuktan
çıkmanın bir yolunun da su komutları vermek oldugunu söylemistik:
>>> import sys; sys.exit()
Bu komutu tek satırda yazmıstık, ama istersek söyle de yazabiliriz elbette:
6.5. Birkaç Pratik Bilgi 69
Python 3 için Türkçe Kılavuz, Sürüm 3
>>> import sys
>>> sys.exit()
Dedik ya, sys modülü içinde pek çok degisken ve fonksiyon bulunur. Nasıl stdout sys modülü
içindeki degiskenlerden biri ise, exit() de sys modülü içinde bulunan fonksiyonlardan biridir.
Biz ‘modüller’ konusunu ilerleyen derslerde ayrıntılı bir sekilde inceleyecegiz. Simdilik
modüllere iliskin olarak yalnızca sunları bilelim yeter:
1. Python’da modüller import komutu ile içe aktarılır. Örnegin sys adlı modülü içe aktarmak
için import sys komutunu veriyoruz.
2. Modüller içinde pek çok faydalı degisken ve fonksiyon bulunur. Iste bir modülü içe
aktardıgımızda, o modül içindeki bu degisken ve fonksiyonları kullanma imkanı elde ederiz.
3. sys modülü içindeki degiskenlere bir örnek stdout ; fonksiyonlara örnek
ise exit() fonksiyonudur. Bir modül içindeki bu degisken ve fonksiyonlara
‘modül_adı.degisken_ya_da_fonksiyon’ formülünü kullanarak erisebiliriz. Örnegin:
>>> sys.stdout
>>> sys.exit()
4. Hatırlarsanız bundan önce de, open() fonksiyonu ile dosya olusturmayı anlatırken,
olusturulan dosyanın hangi dizinde oldugunu bulabilmek amacıyla, o anda içinde
bulundugumuz dizini tespit edebilmek için su kodları kullanmıstık:
>>> import os
>>> os.getcwd()
Burada da os adlı baska bir modül görüyoruz. Iste os da tıpkı sys gibi bir modüldür ve tıpkı
sys modülünde oldugu gibi, os modülünün de içinde pek çok yararlı degisken ve fonksiyon
bulunur. getcwd() adlı fonksiyon da os modülü içinde yer alan ve o anda hangi dizin altında
bulundugumuzu gösteren bir fonksiyondur. Elbette, yine tıpkı sys modülünde oldugu gibi,
os modülü içindeki bu yararlı degisken ve fonksiyonları kullanabilmek için de öncelikle bu os
modülünü içe aktarmamız, yani programımıza dahil etmemiz gerekiyor. os modülünü import
komutu aracılıgıyla uygun bir sekilde içe aktardıktan sonra, modül içinde yer alan getcwd()
adlı fonksiyona yine ‘modül_adı.fonksiyon’ formülünü kullanarak erisebiliyoruz.
Modüllere iliskin simdilik bu kadar bilgi yeter. Modülleri bir kenara bırakıp yolumuza devam
edelim...
Eger sys.exit() komutunu verip etkilesimli kabuktan çıktıysanız, etkilesimli kabuga tekrar
girin ve sys modülünü yeniden içe aktarın:
>>> import sys
Not: Bir modülü aynı etkilesimli kabuk oturumu içinde bir kez içe aktarmak yeterlidir. Bir
modülü bir kez içe aktardıktan sonra, o oturum süresince bu modül içindeki degisken ve
fonksiyonları kullanmaya devam edebilirsiniz. Ama tabii ki etkilesimli kabugu kapatıp tekrar
açtıktan sonra, bir modülü kullanabilmek için o modülü tekrar içe aktarmanız gerekir.
Simdi su kodu yazın:
>>> f = open("dosya.txt", "w")
70 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
Bu kodun anlamını biliyorsunuz. Burada dosya.txt adlı bir dosyayı yazma kipinde açmıs
olduk. Tahmin edebileceginiz gibi, çıktılarımızı ekran yerine bu dosyaya yönlendirecegiz.
Simdi de söyle bir kod yazalım:
>>> sys.stdout = f
Bildiginiz gibi, sys.stdout degeri Python’ın çıktıları hangi konuma verecegini belirliyor. Iste
biz burada sys.stdout ‘un degerini biraz önce olusturdugumuz f adlı dosya ile degistiriyoruz.
Böylece Python bütün çıktıları f degiskeni içinde belirttigimiz dosya.txt adlı dosyaya
gönderiyor.
Bu andan sonra yazacagınız her sey dosya.txt adlı dosyaya gidecektir:
>>> print("deneme metni", flush=True)
Gördügünüz gibi, burada 1le parametresini kullanmadıgımız halde çıktılarımız ekrana degil,
dosya.txt adlı bir dosyaya yazdırıldı. Peki ama bu nasıl oldu? Aslında bunun cevabı çok basit:
Biraz önce sys.stdout = f komutuyla sys.stdout ‘un degerini f degiskeninin tuttugu dosya
ile degistirdik. Bu islemi yapmadan önce sys.stdout‘un degeri suydu hatırlarsanız:
<_io.TextIOWrapper name='<stdout>' mode='w' encoding='cp1254'>
Ama sys.stdout = f komutundan sonra her sey degisti. Kontrol edelim:
>>> print(sys.stdout, flush=True)
Elbette bu komuttan herhangi bir çıktı almadınız. Çıktının ne oldugunu görmek için dosya.txt
adlı dosyayı açın. Orada su satırı göreceksiniz:
<_io.TextIOWrapper name='dosya.txt' mode='w' encoding='cp1254'>
Gördügünüz gibi, özgün stdout çıktısındaki name=’<stdout>’ degeri name=’dosya.txt’ olmus.
Dolayısıyla artık bütün çıktılar dosya.txt adlı dosyaya gidiyor...
Bu arada, yukarıdaki çıktıda görünen name, mode ve encoding degerlerine su sekilde
ulasabilirsiniz:
>>> sys.stdout.name
>>> sys.stdout.mode
>>> sys.stdout.encoding
Burada sys.stdout.name komutu standart çıktı konumunun o anki adını verecektir.
sys.stdout.mode komutu ise standart çıktı konumunun hangi kipe sahip oldugunu gösterir.
Standart çıktı konumu genellikle yazma kipinde (w) bulunur. sys.stdout.encoding kodu
ise standart çıktı konumunun sahip oldugu kodlama biçimini gösterir. Kodlama biçimi,
standart çıktı konumuna yazdıracagınız karakterlerin hangi kodlama biçimi ile kodlanacagını
belirler. Kodlama biçimi Windows’ta genellikle ‘cp1254’, GNU/Linux’ta ise ‘utf-8’dir. Eger
bu kodlama biçimi yanlıs olursa, mesela dosyaya yazdıracagınız karakterler içindeki Türkçe
har2er düzgün görüntülenemez. Eger burada söylediklerimiz size su anda anlasılmaz
geliyorsa, söylediklerimizi dikkate almadan yolunuza devam edebilirsiniz. Birkaç bölüm sonra
bu söylediklerimiz size daha fazla sey ifade etmeye baslayacak nasıl olsa.
Peki standart çıktı konumunu eski haline döndürmek isterseniz ne yapacaksınız? Bunun için
etkilesimli kabuktan çıkıp tekrar girebilirsiniz. Etkilesimli kabugu tekrar açtıgınızda her seyin
eski haline döndügünü göreceksiniz. Aynı sekilde, eger bu kodları bir program dosyasına
yazmıs olsaydınız, programınız kapandıgında her sey eski haline dönecekti.
6.5. Birkaç Pratik Bilgi 71
Python 3 için Türkçe Kılavuz, Sürüm 3
Peki standart çıktı konumunu, etkilesimli kabuktan çıkmadan veya programı kapatmadan eski
haline döndürmenin bir yolu var mı? Elbette var. Dikkatlice bakın:
>>> import sys
>>> f = open("dosya.txt", "w")
>>> sys.stdout, f = f, sys.stdout
>>> print("deneme", flush=True)
>>> f, sys.stdout = sys.stdout, f
>>> print("deneme")
deneme
Uyarı: Eger yukarıdaki kodları çalıstıramıyorsanız, aynı etkilesimli kabuk oturumunda
önceden verdiginiz kodlar bu kodların dogru çıktı vermesini engelliyor olabilir. Bu sorunu
asmak için, etkilesimli kabugu kapatıp tekrar açın ve yukarıdaki komutları tekrar verin.
Aslında burada anlayamayacagınız hiçbir sey yok. Burada yaptıgımız seyi geçen bölümlerde
degiskenlerin degerini nasıl takas edecegimizi anlatırken de yapmıstık. Hatırlayalım:
>>> osman = "Araştırma Geliştirme Müdürü"
>>> mehmet = "Proje Sorumlusu"
>>> osman, mehmet = mehmet, osman
Bu kodlarla Osman ve Mehmet’in unvanlarını birbiriyle takas etmistik. Iste yukarıda
yaptıgımız sey de bununla aynıdır. sys.stdout, f = f, sys.stdout dedigimizde f degerini
sys.stdout ‘a, sys.stdout ‘un degerini ise f ‘ye vermis oluyoruz. f, sys.stdout = sys.stdout,
f dedigimizde ise, bu islemin tam tersini yaparak her seyi eski haline getirmis oluyoruz.
Python’ın bize sundugu bu kolaylıktan faydalanarak degiskenlerin degerini birbiriyle kolayca
takas edebiliyoruz. Eger böyle bir kolaylık olmasaydı yukarıdaki kodları söyle yazabilirdik:
>>> import sys
>>> f = open("dosya.txt", "w")
>>> özgün_stdout = sys.stdout
>>> sys.stdout = f
>>> print("deneme", flush=True)
>>> sys.stdout = özgün_stdout
>>> print("deneme")
deneme
Gördügünüz gibi, sys.stdout ‘un degerini kaybetmemek için, sys.stdout degerini f adlı
dosyaya göndermeden önce su kod yardımıyla yedekliyoruz:
>>> özgün_stdout = sys.stdout
sys.stdout ‘un özgün degerini özgün_stdout degiskenine atadıgımız için, bu degere sonradan
tekrar ulasabilecegiz. Zaten yukarıdaki kodlardan da gördügünüz gibi, sys.stdout ‘un özgün
degerine dönmek istedigimizde su kodu yazarak istegimizi gerçeklestirebiliyoruz:
>>> sys.stdout = özgün_stdout
Böylece stdout degeri eski haline dönmüs oluyor ve bundan sonra yazdırdıgımız her sey
yeniden ekrana basılmaya baslıyor.
...ve böylece uzun bir bölümü daha geride bıraktık. Bu bölümde hem print() fonksiyonunu
bütün ayrıntılarıyla incelemis olduk, hem de Python programlama diline dair baska çok
72 Bölüm 6. print() Fonksiyonu
Python 3 için Türkçe Kılavuz, Sürüm 3
önemli kavramlardan söz ettik. Bu bakımdan bu bölüm bize epey sey ögretti. Artık
ögrendigimiz bu bilgileri de küfemize koyarak basımız dik bir sekilde yola devam edebiliriz.
6.5. Birkaç