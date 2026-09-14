# Koray Öner

**Yazılım geliştirici — Türkiye mevzuatına göre çalışan açık kaynak hesaplama araçları yazıyorum.**

[korayoner.dev](https://korayoner.dev) · [hesap-cekirdegi (npm)](https://www.npmjs.com/package/hesap-cekirdegi)

---

## Ne yapıyorum

[korayoner.dev](https://korayoner.dev) üzerinde **44 hesaplama aracı** ve mevzuat yazısı yayımlıyorum: brüt–net maaş, kıdem ve ihbar tazminatı, gelir vergisi, MTV, ÖTV, kira geliri, işsizlik maaşı, kredi maliyeti.

Bu araçların ortak derdi şu: bir hesaplama aracında hata **sessizdir**. Yanlış bir parametre girilirse sayfa açılmaya devam eder, tablo hizalı görünür, kimse uyarı almaz — yalnızca sonuç yanlıştır. Bu yüzden her yasal parametrenin tek bir kaynağı var ve motorlar **1.713 testle** sabitli. Kanun değiştiğinde testler kırılıyor; sayfa sessizce eskimiyor.

- **Bağımlılık yok, derleme adımı yok.** Aynı kod hem tarayıcıda hem Node.js'te çalışıyor.
- **Hesap yöntemi açık.** Her aracın metodoloji sayfası ve testleri herkese açık.
- **Veri cihazdan çıkmıyor.** Hesaplar tarayıcıda yapılıyor; girdiler sunucuya gitmiyor.

### Öne çıkan araçlar

| Araç | Ne yapıyor |
|---|---|
| [Brüt Net Maaş Hesaplama](https://korayoner.dev/maas-hesaplama/) | 12 aylık bordro, kümülatif vergi dilimi etkisiyle |
| [Kıdem ve İhbar Tazminatı](https://korayoner.dev/kidem-tazminati-hesaplama/) | Tavan sınırı ve damga vergisi dahil |
| [İşten Ayrılma Çıkış Paketi](https://korayoner.dev/isten-ayrilma-hesaplama/) | Kıdem, ihbar, izin ve işsizlik ödeneği birlikte |
| [MTV Hesaplama](https://korayoner.dev/mtv-hesaplama/) | Üç tarife ayrı: 2018 öncesi/sonrası tescil ve motosiklet |
| [Araç ÖTV Hesaplama](https://korayoner.dev/otv-hesaplama/) | Hibrit ve şarj edilebilir hibrit koşulları dahil |
| [Kira Geliri Vergisi](https://korayoner.dev/kira-geliri-vergisi-hesaplama/) | İstisna, beyan sınırı, götürü ve gerçek gider |
| [İşsizlik Maaşı](https://korayoner.dev/issizlik-maasi-hesaplama/) | Taban ve tavan sınırlarıyla |
| [Gümrük Vergisi](https://korayoner.dev/gumruk-vergisi-hesaplama/) | Yurt dışı alışverişte toplam maliyet |
| [Kredi Maliyeti](https://korayoner.dev/kredi-hesaplama/) | Yıllık maliyet oranı (YMO) ve gerçek toplam ödeme |

Tamamı: [korayoner.dev](https://korayoner.dev)

### Yazılar

Mevzuat değiştiğinde ne olduğunu, aracın verdiği sayının **neden** o sayı olduğunu anlatıyorum.

- [Torba Yasa 2026–2027: Ne Var, Ne Yok](https://korayoner.dev/makaleler/torba-yasa-ne-var-ne-yok/)
- [Kademeli Emeklilik Son Durum](https://korayoner.dev/makaleler/kademeli-emeklilik-son-durum/)
- [Maaşım Neden Düştü? Vergi Dilimi Etkisi](https://korayoner.dev/makaleler/maasim-neden-dustu/)
- [Hepsi →](https://korayoner.dev/makaleler/)

---

## Açık kaynak

**[hesap-cekirdegi](https://github.com/onerkoray/hesap-cekirdegi)** — sitedeki araçların altında çalışan hesap motoru, ayrı bir paket olarak.

```bash
npm install hesap-cekirdegi
```

```js
const Bordro = require("hesap-cekirdegi/bordro/motor.js");

const yil = Bordro.hesaplaYil(60000, 2026);   // 60.000 TL brüt
yil.aylar[0].net;    // Ocak neti
yil.aylar[11].net;   // Aralık neti — kümülatif vergi yüzünden daha düşük
```

Bağımlılıksız, MIT, 1.713 testle sabitli. Bordro, tazminat, emeklilik, kira geliri, kredi ve vergi hesapları.

Diğer projeler: **[keymint](https://github.com/onerkoray/keymint)** (parola üreteci ve güç testi) · **[dither-studio](https://github.com/onerkoray/dither-studio)** (görsel dithering) · **[decorpalette](https://github.com/onerkoray/decorpalette)** (renk paleti)

---

## About me

I'm a software developer building **open-source calculation tools for Turkish tax and labour legislation** — payroll, severance, income tax, vehicle tax, rental income and credit cost.

The problem these tools solve is that errors in a calculator are **silent**: get one legal parameter wrong and the page still renders, the table still lines up, and only the answer is wrong. So every legal parameter has a single source and the engines are pinned by **1,713 tests** that break when the law changes.

The engine is published as [`hesap-cekirdegi`](https://www.npmjs.com/package/hesap-cekirdegi) — dependency-free, no build step, the same code in the browser and in Node.js, MIT licensed.

---

## Bağlantılar

[Web sitesi](https://korayoner.dev) · [Hakkımda](https://korayoner.dev/hakkimda/) · [LinkedIn](https://www.linkedin.com/in/korayoner/) · [X](https://x.com/koraonerdev) · [Substack](https://korayoner.substack.com/) · [Medium](https://onerkoray.medium.com/) · [Instagram](https://www.instagram.com/korayonerv/)

İletişim: [iletisim@korayoner.dev](mailto:iletisim@korayoner.dev)
