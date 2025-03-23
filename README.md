
# 🔬 LLM Fine-Tuning with Hugging Face, PEFT, and Gradio

Bu proje, büyük dil modellerinin (LLM) düşük maliyetli ve verimli bir şekilde fine-tune edilmesini amaçlamaktadır. Google Colab üzerinde Gradio arayüzü desteğiyle model eğitimi ve test aşamaları kullanıcı dostu bir şekilde entegre edilmiştir.

---

## 🚀 Proje Özeti

Notebook, Hugging Face ekosistemini kullanarak `transformers`, `datasets`, `peft`, ve `accelerate` kütüphaneleriyle aşağıdaki işlemleri kapsamaktadır:

- Veriseti hazırlığı ve işlenmesi
- PEFT (Parameter-Efficient Fine-Tuning) kullanılarak modelin yeniden eğitimi
- Gradio ile demo oluşturulması
- Hugging Face Hub'a model yükleme desteği

---

## 🧰 Kullanılan Teknolojiler ve Kütüphaneler

| Kütüphane           | Açıklama                                      |
|--------------------|-----------------------------------------------|
| `transformers`     | Hugging Face modelleri ve tokenizer desteği   |
| `datasets`         | Veriseti yükleme ve işleme                    |
| `peft`             | Verimli parameter tuning (LoRA, QLoRA)        |
| `accelerate`       | Donanım hızlandırmalı eğitim                  |
| `gradio`           | Etkileşimli web arayüzü oluşturma             |
| `huggingface_hub`  | Model paylaşımı ve yükleme                    |

---

## 📂 Veriseti

> Not: Kendi verisetinizi kullanmak için `datasets.load_dataset()` fonksiyonu üzerinden `.csv`, `.json` veya Hugging Face Dataset Hub kullanılabilir.

Notebook şu anda [örnek bir Türkçe verisetini] kullanmaktadır ve belirli bir konu üzerine (örneğin sürdürülebilirlik, hukuk vb.) eğitilmek üzere hazırlanmıştır.

---

## 🧠 Eğitim Detayları

- **Model:** (örneğin) `deepseek-ai/deepseek-llm-7b`
- **Fine-Tuning Yöntemi:** LoRA (Low-Rank Adaptation)
- **Eğitim Platformu:** Google Colab (T4 / A100 GPU)
- **Batch Size:** Ayarlanabilir
- **Epochs:** 3 (ayarlanabilir)
- **Optimizer:** AdamW

---

## ⚙️ Çalıştırma Adımları

### 1. Gerekli kütüphaneleri yükleyin:
```bash
pip install transformers datasets accelerate peft gradio huggingface_hub
```

### 2. Notebook'u çalıştırın:
Google Colab'da adım adım cell'leri takip ederek:

- Veriseti yükleme
- Tokenizer ve model başlatma
- PEFT ile fine-tuning
- Gradio UI ile test etme
- Hugging Face'e model yükleme

---

## 🌐 Gradio Demo

Notebook sonunda aşağıdaki gibi bir demo arayüzü oluşturulmaktadır:

- Input: Serbest metin giriş alanı
- Output: Model çıktısı
- Kullanım: Web üzerinden kolayca test edilebilir

---

## 📈 Sonuçlar ve Değerlendirme

Eğitim sonrası model, özellikle Türkçe dilinde belirli görevlerde başarılı sonuçlar vermektedir. Ek olarak, LoRA tekniği sayesinde düşük VRAM kullanımıyla yüksek doğruluk elde edilmiştir.

> TensorBoard veya Weights & Biases entegrasyonu ile daha detaylı takip eklenebilir.

---

## 📤 Modeli Hugging Face'e Yükleme

```python
from huggingface_hub import login
login(token="hf_...")  # Hugging Face Access Token

trainer.push_to_hub()
tokenizer.push_to_hub()
```

---

## 🤝 Katkı Sağlama

Her türlü katkıya açığız! Lütfen `pull request` gönderin veya `issue` açın. Yeni veriseti entegrasyonu veya model denemeleri yapılabilir.

---

## 📜 Lisans

Bu proje MIT Lisansı ile lisanslanmıştır. Detaylar için `LICENSE` dosyasını inceleyin.

---

## 👤 Yazar

**BAU**  
AI | NLP | LLM Training | Hugging Face & Transformers  
GitHub: [github.com/NoirZangetsu](https://github.com/NoirZangetsu)
