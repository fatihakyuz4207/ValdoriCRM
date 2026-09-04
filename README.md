# Valdori CRM

Sağlık turizmi operasyonu için hasta alımı, danışman ataması, anlaşmalı hastaneye yönlendirme ve takip CRM’i.

Valdori yurtdışı hastaları WhatsApp veya e-posta ile alır, satış danışmanına aktarır, anlaşmalı hastaneye iletir ve işlemi kapanana kadar takip eder. Bu uygulama o akışın çalışan bir dilimidir: gelen kutu, havuz dağıtımı, pipeline, gecikmiş arama kuyruğu ve satış kaydı.

Veriler tarayıcıda tutulur (localStorage). WhatsApp Business API ve kurumsal e-posta henüz bağlanmadı; gelen kutusu bu kanalları simüle eder.

## Çalıştırma

```bash
npm install
npm run dev
```

Tarayıcıda [http://127.0.0.1:43147](http://127.0.0.1:43147) adresini açın.

## Ne yapılır

1. **Gelen kutusu** — WhatsApp / e-posta talebini lead olarak açın, dilerseniz danışman atayın.
2. **Pipeline** — Havuz → iletişim → doktor incelemesi → teklif → onay → hastane → tedavi.
3. **Havuza dağıt** — Atanmamış lead’leri çevrimiçi ve en az yüklü danışmanlara paylaştırır.
4. **Takip kuyruğu** — Gecikmiş / kritik aramaları notla kapatın.
5. **Hastane** — Lead kartından anlaşmalı kliniği seçince dosya iletilmiş sayılır.
6. **Satış** — Hastane atandıktan sonra ciroyu kaydedin.

Demo verisini Satışlar sayfasındaki düğmeyle sıfırlayabilirsiniz.
