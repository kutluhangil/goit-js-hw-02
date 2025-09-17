<h1>📘 JavaScript Ödevleri</h1>

<p>Bu repo, JavaScript öğrenme sürecinde verilen <b>4 görev</b> çözümünü içermektedir. Her görev ayrı bir dosyada (<code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code>, <code>task-4.js</code>) uygulanmıştır.</p>

<hr/>

<h2>🔹 Görev 1: Droid Siparişleri (<code>task-1.js</code>)</h2>
<p>Tamir droidleri sipariş sistemi için bir fonksiyon yazıldı.</p>

<pre>
function makeTransaction(quantity, pricePerDroid, customerCredits) {
  const totalPrice = quantity * pricePerDroid;

  if (totalPrice > customerCredits) {
    return "Insufficient funds!";
  }

  return `You ordered ${quantity} droids worth ${totalPrice} credits!`;
}
</pre>

<h3>✅ Test Sonuçları</h3>
<pre>
makeTransaction(5, 3000, 23000) → "You ordered 5 droids worth 15000 credits!"
makeTransaction(3, 1000, 15000) → "You ordered 3 droids worth 3000 credits!"
makeTransaction(10, 5000, 8000) → "Insufficient funds!"
makeTransaction(8, 2000, 10000) → "Insufficient funds!"
makeTransaction(10, 500, 5000) → "You ordered 10 droids worth 5000 credits!"
</pre>

<hr/>

<h2>🔹 Görev 2: Mesaj Biçimlendirme (<code>task-2.js</code>)</h2>
<p>Metin, maksimum uzunluğu aşıyorsa kesilip <code>...</code> eklenir.</p>

<pre>
function formatMessage(message, maxLength) {
  if (message.length <= maxLength) {
    return message;
  }
  return message.slice(0, maxLength) + "...";
}
</pre>

<h3>✅ Test Sonuçları</h3>
<pre>
formatMessage("Curabitur ligula sapien", 16) → "Curabitur ligula..."
formatMessage("Curabitur ligula sapien", 23) → "Curabitur ligula sapien"
formatMessage("Vestibulum facilisis purus nec", 20) → "Vestibulum facilisis..."
formatMessage("Vestibulum facilisis purus nec", 30) → "Vestibulum facilisis purus nec"
formatMessage("Nunc sed turpis a felis in nunc fringilla", 15) → "Nunc sed turpis..."
formatMessage("Nunc sed turpis a felis in nunc fringilla", 41) → "Nunc sed turpis a felis in nunc fringilla"
</pre>

<hr/>

<h2>🔹 Görev 3: Spam Kontrolü (<code>task-3.js</code>)</h2>
<p>Mesajda <b>spam</b> veya <b>sale</b> kelimeleri geçiyorsa <code>true</code>, yoksa <code>false</code> döndürür. Büyük/küçük harf duyarsızdır.</p>

<pre>
function checkForSpam(message) {
  const lowerMessage = message.toLowerCase();
  return lowerMessage.includes("spam") || lowerMessage.includes("sale");
}
</pre>

<h3>✅ Test Sonuçları</h3>
<pre>
checkForSpam("Latest technology news") → false
checkForSpam("JavaScript weekly newsletter") → false
checkForSpam("Get best sale offers now!") → true
checkForSpam("Amazing SalE, only tonight!") → true
checkForSpam("Trust me, this is not a spam message") → true
checkForSpam("Get rid of sPaM emails. Our book in on sale!") → true
checkForSpam("[SPAM] How to earn fast money?") → true
</pre>

<hr/>

<h2>🔹 Görev 4: Teslimat Maliyeti (<code>task-4.js</code>)</h2>
<p>Kullanıcının ülkesine göre teslimat ücretini hesaplar. <code>switch</code> ifadesi kullanılmıştır.</p>

<pre>
function getShippingCost(country) {
  let price;

  switch (country) {
    case "China":
      price = 100;
      break;
    case "Chile":
      price = 250;
      break;
    case "Australia":
      price = 170;
      break;
    case "Jamaica":
      price = 120;
      break;
    default:
      return "Sorry, there is no delivery to your country";
  }

  return `Shipping to ${country} will cost ${price} credits`;
}
</pre>

<h3>✅ Test Sonuçları</h3>
<pre>
getShippingCost("Australia") → "Shipping to Australia will cost 170 credits"
getShippingCost("Germany") → "Sorry, there is no delivery to your country"
getShippingCost("China") → "Shipping to China will cost 100 credits"
getShippingCost("Chile") → "Shipping to Chile will cost 250 credits"
getShippingCost("Jamaica") → "Shipping to Jamaica will cost 120 credits"
getShippingCost("Sweden") → "Sorry, there is no delivery to your country"
</pre>

<hr/>

<h2>📌 Özet</h2>
<ul>
  <li><b>Görev 1:</b> Droid sipariş sistemi</li>
  <li><b>Görev 2:</b> Mesaj biçimlendirme</li>
  <li><b>Görev 3:</b> Spam kontrolü</li>
  <li><b>Görev 4:</b> Teslimat maliyeti</li>
</ul>
