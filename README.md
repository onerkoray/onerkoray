# Koray Öner

**Yazılım geliştirici. Türkiye mevzuatına göre çalışan, açık kaynak ve testli hesaplama araçları yazıyorum.**

[korayoner.dev](https://korayoner.dev) · [Koray Öner kimdir?](https://korayoner.dev/hakkimda/) · [Çalışma dizini](https://korayoner.dev/koray-oner/) · [Yayınlar (DOI)](https://korayoner.dev/yayinlar/) · [ORCID 0009-0005-8730-3577](https://orcid.org/0009-0005-8730-3577)

---

## Ne yapıyorum

[korayoner.dev](https://korayoner.dev) üzerinde maaş, vergi, SGK, emeklilik ve kredi için ücretsiz hesaplama araçları ve bu araçların arkasındaki mevzuatı anlatan yazılar yayımlıyorum. Güncel sayılar ve tam liste [çalışma dizininde](https://korayoner.dev/koray-oner/).

Bu araçların ortak derdi şu: bir hesaplama aracında hata **sessizdir**. Yanlış bir parametre girilirse sayfa açılmaya devam eder, tablo hizalı görünür, kimse uyarı almaz; yalnızca sonuç yanlıştır. Bu yüzden her yasal parametrenin tek bir kaynağı var, motorlar ve yazılardaki her rakam otomatik testlerle sabitli. Kanun değiştiğinde testler kırılıyor; sayfa sessizce eskimiyor.

- **Bağımlılık yok, derleme adımı yok.** Aynı kod hem tarayıcıda hem Node.js'te çalışıyor.
- **Hesap yöntemi açık.** Her aracın yöntemi ve testleri herkese açık.
- **Veri cihazdan çıkmıyor.** Hesaplar tarayıcıda yapılıyor; girdiler sunucuya gitmiyor.

### Öne çıkan araçlar

| Araç | Ne yapıyor |
|---|---|
| [Brüt Net Maaş Hesaplama](https://korayoner.dev/maas-hesaplama/) | 12 aylık bordro, kümülatif vergi dilimi etkisiyle |
| [Ne Zaman Emekli Olurum?](https://korayoner.dev/ne-zaman-emekli-olurum/) | EYT, 1999–2008 ve 2008 sonrası; borçlanmanın etkisi |
| [Rapor Parası Hesaplama](https://korayoner.dev/rapor-parasi-hesaplama/) | Hastalık, iş kazası ve doğum raporunda SGK ödeneği ve raporlu ayın neti |
| [Engelli Araç ÖTV İstisnası](https://korayoner.dev/engelli-arac-otv-istisnasi-hesaplama/) | Uygunluk, fiyat sınırı, yerli katkı, on yıl kuralı ve MTV |
| [Kıdem ve İhbar Tazminatı](https://korayoner.dev/kidem-tazminati-hesaplama/) | Tavan sınırı ve damga vergisi dahil |
| [İşten Ayrılma Paketi](https://korayoner.dev/isten-ayrilma-hesaplama/) | Kıdem, ihbar, izin ve işsizlik ödeneği birlikte |
| [Bordro Denetimi](https://korayoner.dev/bordro-denetim/) | Bordronuzdaki rakamları yeniden hesaplayıp farkı gösterir |
| [Araç ÖTV](https://korayoner.dev/otv-hesaplama/) ve [MTV](https://korayoner.dev/mtv-hesaplama/) | Hibrit, şarj edilebilir hibrit ve elektrikli satırları dahil |
| [Kira Geliri Vergisi](https://korayoner.dev/kira-geliri-vergisi-hesaplama/) | İstisna, beyan sınırı, götürü ve gerçek gider |
| [Kredi Maliyeti](https://korayoner.dev/kredi-hesaplama/) | Yıllık maliyet oranı ve gerçek toplam ödeme |

Tamamı: [korayoner.dev](https://korayoner.dev/#projects)

### Yazılar

Mevzuat değiştiğinde ne olduğunu, aracın verdiği sayının **neden** o sayı olduğunu anlatıyorum. Yazılardaki her rakam testle yeniden hesaplanıyor.

- [Doğum Parası Ne Kadar? 24 Haftalık İznin Hesabı](https://korayoner.dev/makaleler/dogum-parasi-ne-kadar/)
- [Ocak 2027'yi Meclis mi Belirleyecek?](https://korayoner.dev/makaleler/ocak-2027-meclis-mi-belirleyecek/)
- [Torba Yasa: Ne Var, Ne Yok](https://korayoner.dev/makaleler/torba-yasa-ne-var-ne-yok/)
- [Kademeli Emeklilik Son Durum](https://korayoner.dev/makaleler/kademeli-emeklilik-son-durum/)
- [Maaşım Neden Düştü?](https://korayoner.dev/makaleler/maasim-neden-dustu/)
- [Hepsi →](https://korayoner.dev/makaleler/)

### Yayımlanmış çalışmalar

Vergi kaması, dilim kayması, emeklilik finansmanı ve banka kârlılığı üzerine DOI'li, açık erişimli çalışmalar: [korayoner.dev/yayinlar](https://korayoner.dev/yayinlar/).

---

## Açık kaynak

**[hesap-cekirdegi](https://github.com/onerkoray/hesap-cekirdegi)**: sitedeki araçların altında çalışan hesap motoru, ayrı bir paket olarak.

```bash
npm install hesap-cekirdegi
```

```js
const Bordro = require("hesap-cekirdegi/bordro/motor.js");

const yil = Bordro.hesaplaYil(60000, 2026);   // 60.000 TL brüt
yil.aylar[0].net;    // Ocak neti
yil.aylar[11].net;   // Aralık neti: kümülatif vergi yüzünden daha düşük
```

Bağımlılıksız, MIT lisanslı, testlerle sabitli. Bordro, tazminat, emeklilik, kira geliri, kredi ve vergi hesapları.

---

## About me

I'm **Koray Öner**, a software developer building **open-source calculation tools for Turkish tax and labour legislation**: payroll, severance, retirement, sick and maternity pay, income tax, vehicle tax, rental income and credit cost.

The problem these tools solve is that errors in a calculator are **silent**: get one legal parameter wrong and the page still renders, the table still lines up, and only the answer is wrong. So every legal parameter has a single source and the engines are pinned by automated tests that break when the law changes.

The engine is published as [`hesap-cekirdegi`](https://www.npmjs.com/package/hesap-cekirdegi): dependency-free, no build step, the same code in the browser and in Node.js, MIT licensed. Research notes with DOIs: [korayoner.dev/yayinlar](https://korayoner.dev/yayinlar/).

---

## Bağlantılar

[Web sitesi](https://korayoner.dev) · [Hakkımda](https://korayoner.dev/hakkimda/) · [ORCID iD 0009-0005-8730-3577](https://orcid.org/0009-0005-8730-3577) · [LinkedIn](https://www.linkedin.com/in/korayoner/) · [X](https://x.com/korayonerdev) · [YouTube](https://www.youtube.com/@onerkoray) · [Substack](https://korayoner.substack.com/) · [Medium](https://onerkoray.medium.com/) · [Instagram](https://www.instagram.com/korayonerv/)

İletişim: [iletisim@korayoner.dev](mailto:iletisim@korayoner.dev)
