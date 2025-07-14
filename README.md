# TurkVideoSum - turkish-youtube-text-summarization
This repository provides a dataset for training and testing LLMs on summarization of Turkish Youtube videos' transcripts.

Bu veri seti, Youtube Türkiye'nin farklı kategorilerde en çok takip edilen kanalları tarafından yüklenmiş 650 Türkçe videonun başta metni ve özeti (abstractive summary) olmak üzere çeşitli bilgilerini içermektedir. Veri setinin amacı, dil modellerini Türkçe Youtube videolarının metinlerini özetlemek için eğitmek ve test etmektir. Veri seti, üç ayrı json dosyasından oluşur: train.json (training data), validation.json (validation data) ve test.json (test data). Bu dosyalardaki videoların dağılımı şu şekildedir: 520, 65, 65.

## Farklı Kategoriler ile Daha Zengin Bir Veri Seti
Bu veri seti; eğlence, spor, podcast, oyun, tarih, gezi, bilim/teknoloji, belgesel, haber, kişisel gelişim, film/dizi, skeç, magazin ve felsefe gibi birçok farklı kategoriden videolar içermektedir. Böylece bu veri setinde eğitilen dil modelleri, Türkçe metin özetlemeyi daha genel bir biçimde öğrenecektir. Ayrıca performans ölçmek için kullanılan test veri seti, Türkçe metin özetleme için daha kapsayıcı ve gerçekçi bir benchmark olacaktır.

## İçerik
Veri seti, başta videoların metni ve özeti olmak üzere videoların başlığını, kategorisini, süresini, hangi kanal tarafından yüklendiğini ve url'sini içermektedir. Videoların metinleri, çoğunlukla OpenAI'nın Whisper ses tanımlama modeliyle üretilmiş, bir kısmı ise Youtube'nin kendi sağladığı transkriptlerden elde edilmiştir. Yazım ve imla hataları, farklı dil modelleri kullanılarak olabildiğince düzeltilmiş ve meydana gelen tekrarlama halüsinasyonları tek tek çıkarılmıştır. Video özetleri ise Gemini 2.5-Flash başta olmak üzere Grok 3 gibi dil modelleriyle oluşturulmuştur. Üretilen özetler, tek tek incelenmiştir.
