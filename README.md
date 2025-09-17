<h1>📘 JavaScript Homework 2</h1>

<p>This repository contains solutions for <b>4 tasks</b> focused on <b>branching</b> and <b>loops</b> in JavaScript. Each task is implemented in a separate file (<code>task-1.js</code>, <code>task-2.js</code>, <code>task-3.js</code>, <code>task-4.js</code>).</p>

<hr/>

<h2>🔹 Task 1: Droid Orders (<code>task-1.js</code>)</h2>
<p>A function was written to handle a droid ordering system with credit validation.</p>

<pre>
function makeTransaction(quantity, pricePerDroid, customerCredits) {
  const totalPrice = quantity * pricePerDroid;

  if (totalPrice > customerCredits) {
    return "Insufficient funds!";
  }

  return `You ordered ${quantity} droids worth ${totalPrice} credits!`;
}
</pre>

<h3>✅ Test Results</h3>
<pre>
makeTransaction(5, 3000, 23000) → "You ordered 5 droids worth 15000 credits!"
makeTransaction(3, 1000, 15000) → "You ordered 3 droids worth 3000 credits!"
makeTransaction(10, 5000, 8000) → "Insufficient funds!"
makeTransaction(8, 2000, 10000) → "Insufficient funds!"
makeTransaction(10, 500, 5000) → "You ordered 10 droids worth 5000 credits!"
</pre>

<hr/>

<h2>🔹 Task 2: Message Formatting (<code>task-2.js</code>)</h2>
<p>The function trims long messages and appends <code>...</code> if they exceed a given length.</p>

<pre>
function formatMessage(message, maxLength) {
  if (message.length <= maxLength) {
    return message;
  }
  return message.slice(0, maxLength) + "...";
}
</pre>

<h3>✅ Test Results</h3>
<pre>
formatMessage("Curabitur ligula sapien", 16) → "Curabitur ligula..."
formatMessage("Curabitur ligula sapien", 23) → "Curabitur ligula sapien"
formatMessage("Vestibulum facilisis purus nec", 20) → "Vestibulum facilisis..."
formatMessage("Vestibulum facilisis purus nec", 30) → "Vestibulum facilisis purus nec"
formatMessage("Nunc sed turpis a felis in nunc fringilla", 15) → "Nunc sed turpis..."
formatMessage("Nunc sed turpis a felis in nunc fringilla", 41) → "Nunc sed turpis a felis in nunc fringilla"
</pre>

<hr/>

<h2>🔹 Task 3: Spam Check (<code>task-3.js</code>)</h2>
<p>The function checks if the message contains banned words <b>spam</b> or <b>sale</b> (case-insensitive).</p>

<pre>
function checkForSpam(message) {
  const lowerMessage = message.toLowerCase();
  return lowerMessage.includes("spam") || lowerMessage.includes("sale");
}
</pre>

<h3>✅ Test Results</h3>
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

<h2>🔹 Task 4: Shipping Cost (<code>task-4.js</code>)</h2>
<p>The function determines shipping availability and calculates cost by country using a <code>switch</code> statement.</p>

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

<h3>✅ Test Results</h3>
<pre>
getShippingCost("Australia") → "Shipping to Australia will cost 170 credits"
getShippingCost("Germany") → "Sorry, there is no delivery to your country"
getShippingCost("China") → "Shipping to China will cost 100 credits"
getShippingCost("Chile") → "Shipping to Chile will cost 250 credits"
getShippingCost("Jamaica") → "Shipping to Jamaica will cost 120 credits"
getShippingCost("Sweden") → "Sorry, there is no delivery to your country"
</pre>

<hr/>

<h2>📌 Summary & Reflection</h2>

<p>Great job! 💪  
Now it's time to summarize and reflect on what you learned in Module 2.</p>

<p>Now you know:</p>
<ul>
  <li>How branching works: <code>if</code> statements, <code>switch</code> operator, ternary operator</li>
  <li>Logical operators: <code>&&</code>, <code>||</code>, <code>!</code></li>
  <li>String methods: <code>slice()</code>, <code>toLowerCase()</code>, <code>toUpperCase()</code>, <code>includes()</code>, <code>startsWith()</code>, <code>endsWith()</code>, <code>indexOf()</code>, <code>trim()</code></li>
  <li>Loops: <code>while</code>, <code>do…while</code>, <code>for</code></li>
</ul>

<p>It’s time to reinforce this knowledge with practice and also review what you learned in the previous module.</p>

<hr/>

<h2>📌 Overview</h2>
<ul>
  <li><b>Task 1:</b> Droid order system with credit check</li>
  <li><b>Task 2:</b> Message formatting with length limit</li>
  <li><b>Task 3:</b> Spam detection in text</li>
  <li><b>Task 4:</b> Shipping cost calculation by country</li>
</ul>
