
PID (Process Identification)
PID, süreç kimliği (Process Identification) bir süreç için benzersiz bir numaradır. Bu numara, sistem üzerinde çalışan her süreç için benzersiz olarak atanır ve sistem tarafından kullanılır. Bir işlemi başlatmak veya bitirmek için kullanılır ayrıca işlem devam ederken çalışma durumunu kontrol etmemizi sağlar.

kill()
Bu fonksiyon, herhangi bir islem veya islem grubuna sinyal gondermek icin kullanilir.

signal()
Bu fonksiyon sinyal olaylarını işlemek için kullanılabilir. Örneğin, bir programda belirli bir sinyal gerçekleştiğinde belirli bir işlem yapmak isteyebilirsiniz ve bu durumda signal() fonksiyonunu kullanabilirsiniz. Bu fonksiyon, sinyal gerçekleştiğinde çağırılacak olan fonksiyonun adresini sisteme bildirir.Sinyal fonksiyonu iki argüman alır.

Signal vs Sigaction
signal() fonksiyonu sinyal isleyici yurutulurken tekrar sinyal alinmasini engellemez fakat, sigaction sinyal isleyici yurutulurken tekrar sinyal alinmasini engeller ve bu reetrancy problemlerinin onune gecer.
signal()'de portability sorunlari varken, sigaction()'da portability sorunlari yoktur. Portability, farkli isletim sistemlerinde calisabilmek olarak dusunulebilir.
Reetrancy Nedir?

Reentrancy sorunu, bir fonksiyonun kendisini tekrar çağırması ya da başka bir fonksiyon tarafından çağırılması sırasında oluşabilecek sorunları ifade eder. Özellikle, fonksiyon çalışmaya devam ederken, başka bir fonksiyon çağrılabilir ve bu ikinci çağrı fonksiyonun çalışmasını etkileyebilir. Bu, programın beklenmedik şekilde çalışmasına veya çökmesine yol açabilir.

Reentrancy sorunları sinyal işlemlerinde de oluşabilir. Örneğin, bir sinyal işlemi sırasında, çağrılan fonksiyon çalışmaya devam ederken, başka bir sinyal işlemi gerçekleşebilir. Bu, sinyal işlemi sırasında çağrılan fonksiyonun beklenmedik şekilde çalışmasına yol açabilir.

pause()
pause() fonksiyonu, programın çalışmasını askıya alır ve sinyal olayı gerçekleşene kadar bekler. Eğer bir sinyal olayı gerçekleşirse, program çalışmaya devam eder. Bu fonksiyon işlem gerçekleştiğinde sinyal olayı gerçekleştiği için 0 döndürür, eğer işlem gerçekleşmedi ise -1 döndürür.


usleep()
C dilinde usleep() fonksiyonu, UNIX ve benzeri işletim sistemlerinde belirli bir zaman aralığı için uyku modunda beklemek için kullanılan bir fonksiyondur. Bu fonksiyon, <unistd.h> kütüphanesinde tanımlıdır.
usleep() fonksiyonu, verilen miktarda mikrosaniye cinsinden bir zaman aralığı için uyku modunda bekler. Örneğin, aşağıdaki kod satırı, programın 1 saniye (1000000 mikrosaniye) boyunca uyku modunda beklemesini sağlar.


