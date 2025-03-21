Ankara Metro Simülasyonu

Proje Açıklaması

Bu proje, Ankara'daki metro ağı içerisinde iki istasyon arasındaki en hızlı ve en az aktarmalı rotayı bulmayı amaçlayan bir Python simülasyonudur. Projede gerçek dünya problemlerine çözüm üretmek adına graf veri yapısı ve algoritmalar kullanılmıştır.

Kullanılan Teknolojiler ve Kütüphaneler

- Python 3.x : Projenin ana programlama dili.
- collections: deque yapısı ile BFS algoritmasında kuyruk yönetimi için kullandım.
- heapq: Öncelik kuyruğu (min-heap) oluşturarak A* algoritmasında en kısa süreli yolları hızlıca seçebilmek için kullandım.


Algoritmaların Çalışma Mantığı


BFS Algoritması (en az aktarmalı rota)

- BFS, graf yapısında katman katman gezerek hedefe en kısa aktarma yolu buluyor.
- İlk olarak başlangıç istasyonu kuyruk yapısına eklenir.
- Kuyrukta her adımda bir istasyon ve onun yol bilgisi tutulur.
- Komşu istasyonlar ziyaret edilerek hedef istasyona ulaşılana kadar ilerlenir.
- İlk hedefe ulaşıldığında o yol döndürülür, böylece en az aktarma sağlanır.

A* Algoritması (en hızlı rota)

- A* algoritması, graf üzerinde toplam süre bilgisini minimize eden bir yol bulma algoritmasıdır.
- Burada, heapq ile her adımda toplam süresi en düşük olan yol seçilir.
- Her istasyon için süre birikerek öncelik kuyruğuna eklenir.
- Hedef istasyona ulaşıldığında, o ana kadar geçen toplam süre ve rota döndürülür.


Örnek Kullanım ve Test Sonuçları

Test Senaryoları

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (19 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
En hızlı rota (17 dakika): Keçiören -> Gar -> Sıhhiye -> Kızılay -> AŞTİ


Projeyi Geliştirme Fikirleri

- Metro haritasını görselleştirmek.
- Kullanıcıların istasyon giriş kaydını alıp kalabalığı ölçmek.
- Saatlere göre sefer sıklığını ayarlamak için giriş kayıtlarından bir veritabanı oluşturmak.
- Kullanıcılara metronun kalabalık düzeyini yansıtan bir ekran sunmak.


Bu proje Ankara'nın gerçek problemlerine çözüm üretmek için tasarlanmıştır.


Hazırlayan: Ahmet Yaşar Sözüer
Hazırlanan: Mart 2025, Global AI Hub Python Bootcamp

