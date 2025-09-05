<p align="center">
  <img src="/assets/logo.png" alt="PesaDigital Logo"  /><br>
</p>

<p>
<i>A simple, digital finance tracker built for individuals in developing countries.</i>
</p>



## 🌍 Why PesaDigital?

In many developing countries, managing personal finances is still a challenge due to lack of simple, localized tools. Existing solutions are either too complex, too expensive, or not designed for the realities of everyday individuals.

**PesaDigital** is designed with simplicity and accessibility in mind:
- Easy to record daily income and expenses
- Works offline (self-hosted or on your device)
- Summaries and charts to help you understand your finances
- Lightweight, fast, and built for personal use

---

## ✨ Features

- 📅 **Quick Entry** — Add income or expenses with just a few fields (date, amount, category).  
- 🔄 **Recurring Transactions** — Automatically record repeating expenses or income.  
- 📊 **Visual Summaries** — Pie charts and cashflow graphs for a clear monthly overview.  
- ⚡ **Lightweight & Self-Hosted** — No internet required, your data stays with you.  
- 🌗 **Dark & Light Mode** — Comfortable UI for any device.  
- 📱 **Mobile-Friendly (PWA)** — Install on your phone or desktop for easy access.  

---

## 🚀 Installation

The recommended way is using **Docker**:

```bash
docker run --rm -d \
  --name pesadigital \
  -p 8080:8080 \
  -v pesadigital:/app/data \
  pesadigital:latest
```

Or with **Docker Compose**:

```yaml
services:
  pesadigital:
    image: pesadigital:latest
    restart: unless-stopped
    ports:
      - 5006:8080
    volumes:
      - /home/user/pesadigital:/app/data
```



## 📖 Usage

Once running, access the app in your browser:

* Dashboard → `http://localhost:8080/`
* Expenses Table → `http://localhost:8080/table`
* Settings → `http://localhost:8080/settings`

From here you can:

* Add expenses/income
* View summaries and graphs
* Manage categories and currency symbols
* Import/export your data

---

## 🔒 Note on Security

PesaDigital does not include built-in authentication (to stay lightweight). If deploying online, secure it with a reverse proxy and external authentication (e.g. Nginx Proxy Manager, Authelia). Soon it's will be ready.


## 🌟 Roadmap

* ✅ Core expense/income tracking
* ✅ Graphs and summaries
* 🔜 SMS/USSD support for areas with limited smartphones
* 🔜 Local language support (e.g. Swahili)
* 🔜 Multi-user version for families/groups



<p align="center">💰 Built for financial empowerment in developing countries.</p>
