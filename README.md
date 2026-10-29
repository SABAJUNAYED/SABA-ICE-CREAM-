# SABA-ICE-CREAM-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#123b30">
<title>My Business Book</title>

<style>
:root {
  --green: #123b30;
  --green-light: #1d5745;
  --lime: #c8f169;
  --bg: #f4f6f1;
  --white: #ffffff;
  --ink: #17251f;
  --muted: #718078;
  --line: #e3e9e1;
  --red: #b42318;
}

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  background: var(--bg);
  color: var(--ink);
  font-family: Arial, sans-serif;
}

header {
  background: linear-gradient(125deg, #102f27, #1d5745);
  color: white;
  padding: 28px 22px;
  border-radius: 0 0 26px 26px;
}

.brand {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo {
  width: 48px;
  height: 48px;
  border-radius: 15px;
  background: var(--lime);
  color: var(--green);
  display: grid;
  place-items: center;
  font-size: 24px;
  font-weight: 900;
}

header h1 {
  margin: 0;
  font-size: 24px;
}

header p {
  color: #c8ddd2;
  font-size: 12px;
  margin-bottom: 0;
}

.container {
  max-width: 1000px;
  margin: auto;
  padding: 18px;
}

nav {
  display: flex;
  gap: 7px;
  padding: 5px;
  background: #e8eee6;
  border-radius: 14px;
  margin-bottom: 20px;
}

nav button {
  flex: 1;
  padding: 12px 5px;
  border: none;
  border-radius: 10px;
  background: transparent;
  color: #6d7a71;
  font-weight: bold;
}

nav button.active {
  background: white;
  color: var(--green);
  box-shadow: 0 3px 14px #163e2d12;
}

.cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 12px;
}

.card {
  background: white;
  padding: 17px;
  border: 1px solid var(--line);
  border-radius: 17px;
  margin-bottom: 12px;
  box-shadow: 0 8px 25px #183c2d08;
}

.card small {
  color: var(--muted);
  font-size: 12px;
}

.card h2 {
  font-size: 23px;
  margin-bottom: 0;
  overflow-wrap: anywhere;
}

h3 {
  font-size: 17px;
  margin-top: 0;
}

input,
select {
  width: 100%;
  padding: 12px;
  margin: 6px 0 12px;
  border: 1px solid #d9e2d9;
  background: #fcfdfa;
  border-radius: 10px;
  font-size: 14px;
}

button {
  cursor: pointer;
}

.primary {
  width: 100%;
  padding: 13px;
  border: none;
  border-radius: 11px;
  background: var(--green);
  color: white;
  font-weight: bold;
}

.secondary {
  padding: 10px 13px;
  border: none;
  border-radius: 10px;
  background: #eaf3e7;
  color: var(--green);
  font-weight: bold;
}

.page {
  display: none;
}

.page.active {
  display: block;
}

.item {
  padding: 13px 0;
  border-bottom: 1px solid var(--line);
}

.item:last-child {
  border-bottom: none;
}

.item strong {
  font-size: 14px;
}

.muted {
  color: var(--muted);
  font-size: 12px;
  margin-top: 5px;
}

.amount {
  color: var(--green);
  font-weight: bold;
}

.danger {
  background: #fff0ee;
  color: var(--red);
  border: none;
  border-radius: 8px;
  padding: 8px;
}

.actions {
  display: flex;
  gap: 8px;
  margin-top: 8px;
}

.actions button {
  flex: 1;
}

.summary-row {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  padding: 12px 0;
  border-bottom: 1px solid var(--line);
  font-size: 14px;
}

.note {
  color: var(--muted);
  font-size: 12px;
  line-height: 1.6;
}

@media (min-width: 700px) {
  .cards {
    grid-template-columns: repeat(4, 1fr);
  }

  .two-columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 14px;
  }
}

@media (max-width: 400px) {
  .container {
    padding: 10px;
  }

  nav button {
    font-size: 11px;
  }
}
</style>
</head>

<body>

<header>
  <div class="brand">
    <div class="logo">B.</div>
    <div>
      <h1>My Business Book</h1>
      <p>YOUR BUSINESS, IN GOOD ORDER</p>
    </div>
  </div>
  <p>Track your khata, stock and daily business accounts.</p>
</header>

<div class="container">

<nav>
  <button class="active" onclick="showPage('home',this)">Home</button>
  <button onclick="showPage('customers',this)">Khata</button>
  <button onclick="showPage('stock',this)">Stock</button>
  <button onclick="showPage('accounts',this)">Hisab</button>
</nav>

<section id="home" class="page active">

  <div class="cards">
    <div class="card">
      <small>Total Customer Due</small>
      <h2 id="totalDue">₹0</h2>
    </div>

    <div class="card">
      <small>Stock at Cost</small>
      <h2 id="stockValue">₹0</h2>
    </div>

    <div class="card">
      <small>Total Sales</small>
      <h2 id="totalSales">₹0</h2>
    </div>

    <div class="card">
      <small>Estimated Profit</small>
      <h2 id="profit">₹0</h2>
    </div>
  </div>

  <div class="card">
    <h3>Welcome, Business Owner!</h3>
    <p class="note">
      Manage customers, products, sales, expenses and payments
      from one simple dashboard.
    </p>
    <button class="primary" onclick="showPage('customers')">
      + Add Customer
    </button>
  </div>

  <div class="card">
    <h3>Recent Activity</h3>
    <div id="recentActivity" class="note">
      No activity recorded yet.
    </div>
  </div>

</section>

<section id="customers" class="page">

  <div class="two-columns">
    <div class="card">
      <h3>Add Customer</h3>

      <input id="customerName" placeholder="Customer name">
      <input id="customerPhone" placeholder="Phone number">
      <input id="openingDue" type="number" min="0"
        step="0.01" placeholder="Opening due ₹">

      <button class="primary" onclick="addCustomer()">
        Save Customer
      </button>
    </div>

    <div class="card">
      <h3>Customer Khata</h3>
      <input id="customerSearch"
        placeholder="Search customer..."
        oninput="renderCustomers()">
      <div id="customerList"></div>
    </div>
  </div>

</section>

<section id="stock" class="page">

  <div class="two-columns">
    <div class="card">
      <h3>Add Product</h3>

      <input id="productName" placeholder="Product name">
      <input id="purchasePrice" type="number"
        min="0" step="0.01" placeholder="Purchase price ₹">
      <input id="sellingPrice" type="number"
        min="0" step="0.01" placeholder="Selling price ₹">
      <input id="quantity" type="number"
        min="0" step="1" placeholder="Quantity">

      <button class="primary" onclick="addProduct()">
        Save Product
      </button>
    </div>

    <div class="card">
      <h3>Stock Inventory</h3>
      <input id="productSearch"
        placeholder="Search product..."
        oninput="renderProducts()">
      <div id="productList"></div>
    </div>
  </div>

</section>

<section id="accounts" class="page">

  <div class="two-columns">

    <div>
      <div class="card">
        <h3>Record Sale</h3>

        <select id="saleProduct"></select>

        <input id="saleQuantity" type="number"
          min="1" step="1" value="1"
          placeholder="Quantity">

        <select id="saleType">
          <option value="cash">Cash Sale</option>
          <option value="credit">Credit Sale</option>
        </select>

        <select id="saleCustomer"></select>

        <button class="primary" onclick="recordSale()">
          Record Sale
        </button>
      </div>

      <div class="card">
        <h3>Record Expense</h3>

        <input id="expenseName" placeholder="Expense details">
        <input id="expenseAmount" type="number"
          min="0.01" step="0.01"
          placeholder="Amount ₹">

        <button class="primary" onclick="addExpense()">
          Save Expense
        </button>
      </div>

      <div class="card">
        <h3>Receive Customer Payment</h3>

        <select id="paymentCustomer"></select>

        <input id="paymentAmount" type="number"
          min="0.01" step="0.01"
          placeholder="Payment amount ₹">

        <button class="primary" onclick="receivePayment()">
          Receive Payment
        </button>
      </div>
    </div>

    <div>
      <div class="card">
        <h3>Business Summary</h3>
        <div id="accountSummary"></div>
      </div>

      <div class="card">
        <h3>Backup & Restore</h3>
        <button class="secondary" onclick="backupData()">
          Export Backup
        </button>

        <input type="file" id="backupFile" accept=".json">

        <button class="primary" onclick="restoreData()">
          Import Backup
        </button>

        <p class="note">
          Keep backup files safe. Importing replaces current data.
        </p>
      </div>
    </div>

  </div>

</section>

</div>

<script>
const STORAGE_KEY = "myBusinessBookPremium";

function blankData() {
  return {
    customers: [],
    products: [],
    sales: [],
    expenses: [],
    payments: []
  };
}

let data;

try {
  data = {
    ...blankData(),
    ...JSON.parse(localStorage.getItem(STORAGE_KEY) || "{}")
  };
} catch (error) {
  data = blankData();
}

function money(value) {
  return "₹" + (Number(value) || 0).toLocaleString("en-IN", {
    maximumFractionDigits: 2
  });
}

function makeId() {
  return Date.now().toString(36) +
    Math.random().toString(36).slice(2, 7);
}

function escapeHTML(value) {
  return String(value ?? "").replace(/[&<>"']/g, char => ({
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    '"': "&quot;",
    "'": "&#39;"
  }[char]));
}

function saveData() {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
  renderAll();
}

function showPage(pageId, button) {
  document.querySelectorAll(".page").forEach(page => {
    page.classList.remove("active");
  });

  document.getElementById(pageId).classList.add("active");

  document.querySelectorAll("nav button").forEach(btn => {
    btn.classList.remove("active");
  });

  if (button) {
    button.classList.add("active");
  } else {
    document.querySelectorAll("nav button").forEach(btn => {
      if (btn.getAttribute("onclick").includes(pageId)) {
        btn.classList.add("active");
      }
    });
  }

  renderAll();
}

function customerDue(customer) {
  let balance = Number(customer.opening) || 0;

  data.sales.forEach(sale => {
    if (sale.type === "credit" &&
        sale.customerId === customer.id) {
      balance += sale.total;
    }
  });

  data.payments.forEach(payment => {
    if (payment.customerId === customer.id) {
      balance -= payment.amount;
    }
  });

  return balance;
}

function addCustomer() {
  const name = document.getElementById("customerName").value.trim();
  const phone = document.getElementById("customerPhone").value.trim();
  const openingText = document.getElementById("openingDue").value;
  const opening = Number(openingText) || 0;

  if (!name) {
    alert("Enter customer name.");
    return;
  }

  if (opening < 0) {
    alert("Opening due cannot be negative.");
    return;
  }

  data.customers.push({
    id: makeId(),
    name,
    phone,
    opening
  });

  document.getElementById("customerName").value = "";
  document.getElementById("customerPhone").value = "";
  document.getElementById("openingDue").value = "";

  saveData();
  alert("Customer saved!");
}

function addProduct() {
  const name = document.getElementById("productName").value.trim();
  const costText = document.getElementById("purchasePrice").value;
  const priceText = document.getElementById("sellingPrice").value;
  const qtyText = document.getElementById("quantity").value;

  const cost = Number(costText);
  const price = Number(priceText);
  const qty = Number(qtyText);

  if (!name || costText === "" || priceText === "" ||
      qtyText === "" || cost < 0 || price < 0 ||
      qty < 0 || !Number.isInteger(qty)) {
    alert("Enter valid product details.");
    return;
  }

  data.products.push({
    id: makeId(),
    name,
    cost,
    price,
    qty
  });

  document.getElementById("productName").value = "";
  document.getElementById("purchasePrice").value = "";
  document.getElementById("sellingPrice").value = "";
  document.getElementById("quantity").value = "";

  saveData();
  alert("Product saved!");
}

function recordSale() {
  const productId = document.getElementById("saleProduct").value;
  const product = data.products.find(p => p.id === productId);
  const qty = Number(document.getElementById("saleQuantity").value);
  const type = document.getElementById("saleType").value;
  const customerId = document.getElementById("saleCustomer").value;

  if (!product) {
    alert("Add a product first.");
    return;
  }

  if (!Number.isInteger(qty) || qty < 1 || qty > product.qty) {
    alert("Invalid quantity or insufficient stock.");
    return;
  }

  if (type === "credit" && !customerId) {
    alert("Select a customer for credit sale.");
    return;
  }

  data.sales.push({
    id: makeId(),
    productId: product.id,
    productName: product.name,
    qty,
    total: qty * product.price,
    cost: qty * product.cost,
    type,
    customerId: type === "credit" ? customerId : "",
    date: new Date().toISOString().slice(0, 10)
  });

  product.qty -= qty;

  document.getElementById("saleQuantity").value = 1;

  saveData();
  alert("Sale recorded!");
}

function addExpense() {
  const name = document.getElementById("expenseName").value.trim();
  const amountText = document.getElementById("expenseAmount").value;
  const amount = Number(amountText);

  if (!name || amountText === "" ||
      !Number.isFinite(amount) || amount <= 0) {
    alert("Enter valid expense details.");
    return;
  }

  data.expenses.push({
    id: makeId(),
    name,
    amount,
    date: new Date().toISOString().slice(0, 10)
  });

  document.getElementById("expenseName").value = "";
  document.getElementById("expenseAmount").value = "";

  saveData();
  alert("Expense saved!");
}

function receivePayment() {
  const customerId = document.getElementById("paymentCustomer").value;
  const amountText = document.getElementById("paymentAmount").value;
  const amount = Number(amountText);

  const customer = data.customers.find(c => c.id === customerId);

  if (!customer || amountText === "" ||
      !Number.isFinite(amount) || amount <= 0) {
    alert("Select a customer and enter a valid payment.");
    return;
  }

  if (amount > customerDue(customer)) {
    alert("Payment cannot exceed the current due.");
    return;
  }

  data.payments.push({
    id: makeId(),
    customerId,
    customerName: customer.name,
    amount,
    date: new Date().toISOString().slice(0, 10)
  });

  document.getElementById("paymentAmount").value = "";

  saveData();
  alert("Payment recorded!");
}

function deleteCustomer(id) {
  const hasTransactions =
    data.sales.some(s => s.customerId === id) ||
    data.payments.some(p => p.customerId === id);

  if (hasTransactions) {
    alert("This customer has transactions and cannot be deleted.");
    return;
  }

  if (confirm("Delete this customer?")) {
    data.customers = data.customers.filter(c => c.id !== id);
    saveData();
  }
}

function deleteProduct(id) {
  if (data.sales.some(s => s.productId === id)) {
    alert("This product has sales and cannot be deleted.");
    return;
  }

  if (confirm("Delete this product?")) {
    data.products = data.products.filter(p => p.id !== id);
    saveData();
  }
}

function fillSelect(elementId, options, placeholder) {
  const element = document.getElementById(elementId);
  const previous = element.value;

  element.innerHTML =
    '<option value="">' + escapeHTML(placeholder) + '</option>';

  options.forEach(item => {
    const option = document.createElement("option");
    option.value = item.value;
    option.textContent = item.label;
    element.appendChild(option);
  });

  if (options.some(item => item.value === previous)) {
    element.value = previous;
  }
}

function renderCustomers() {
  const query = (
    document.getElementById("customerSearch").value || ""
  ).toLowerCase();

  const customers = data.customers.filter(customer =>
    (customer.name + " " + customer.phone).toLowerCase().includes(query)
  );

  document.getElementById("customerList").innerHTML =
    customers.length ? customers.map(customer => `
      <div class="item">
        <strong>${escapeHTML(customer.name)}</strong>
        <div class="muted">${escapeHTML(customer.phone || "No phone number")}</div>
        <p class="amount">Due: ${money(customerDue(customer))}</p>
        <div class="actions">
          <button class="secondary"
            onclick="viewLedger('${customer.id}')">View Ledger</button>
          <button class="danger"
            onclick="deleteCustomer('${customer.id}')">Delete</button>
        </div>
      </div>
    `).join("") : '<p class="note">No customers added yet.</p>';

  const options = data.customers.map(customer => ({
    value: customer.id,
    label: customer.name + " — " + money(customerDue(customer))
  }));

  fillSelect("saleCustomer", options, "Select customer");
  fillSelect("paymentCustomer", options, "Select customer");
}

function viewLedger(customerId) {
  const customer = data.customers.find(c => c.id === customerId);
  if (!customer) return;

  const entries = [
    ...data.sales
      .filter(s => s.customerId === customerId && s.type === "credit")
      .map(s => ({
        date: s.date,
        text: "Credit sale: " + s.productName,
        amount: s.total
      })),
    ...data.payments
      .filter(p => p.customerId === customerId)
      .map(p => ({
        date: p.date,
        text: "Payment received",
        amount: -p.amount
      }))
  ];

  const history = entries
    .sort((a, b) => a.date.localeCompare(b.date))
    .map(item => `${item.date} — ${item.text}: ${money(item.amount)}`)
    .join("\n");

  alert(
    customer.name +
    "\nOpening due: " + money(customer.opening) +
    "\n\n" + (history || "No transactions yet.") +
    "\n\nCurrent due: " + money(customerDue(customer))
  );
}

function renderProducts() {
  const query = (
    document.getElementById("productSearch").value || ""
  ).toLowerCase();

  const products = data.products.filter(p =>
    p.name.toLowerCase().includes(query)
  );

  document.getElementById("productList").innerHTML =
    products.length ? products.map(product => `
      <div class="item">
        <strong>${escapeHTML(product.name)}</strong>
        <div class="muted">Quantity: ${product.qty}</div>
        <div class="muted">Purchase: ${money(product.cost)}</div>
        <div class="muted">Selling: ${money(product.price)}</div>
        <p class="amount">Stock value: ${money(product.qty * product.cost)}</p>
        <div class="actions">
          <button class="secondary"
            onclick="adjustStock('${product.id}')">Adjust Stock</button>
          <button class="danger"
            onclick="deleteProduct('${product.id}')">Delete</button>
        </div>
      </div>
    `).join("") : '<p class="note">No products added yet.</p>';

  fillSelect("saleProduct", data.products.map(product => ({
    value: product.id,
    label: product.name + " — " + product.qty + " available"
  })), "Select product");
}

function adjustStock(productId) {
  const product = data.products.find(p => p.id === productId);
  if (!product) return;

  const quantity = prompt("Enter new total stock quantity:", product.qty);
  if (quantity === null) return;

  if (!Number.isInteger(Number(quantity)) || Number(quantity) < 0) {
    alert("Enter a whole number 0 or above.");
    return;
  }

  product.qty = Number(quantity);
  saveData();
}

function renderAccounts() {
  const sales = data.sales.reduce((sum, s) => sum + s.total, 0);
  const cost = data.sales.reduce((sum, s) => sum + s.cost, 0);
  const expenses = data.expenses.reduce((sum, e) => sum + e.amount, 0);
  const credit = data.sales
    .filter(s => s.type === "credit")
    .reduce((sum, s) => sum + s.total, 0);

  const profit = sales - cost - expenses;

  document.getElementById("accountSummary").innerHTML = `
    <div class="summary-row"><span>Total sales</span><strong>${money(sales)}</strong></div>
    <div class="summary-row"><span>Cash sales</span><strong>${money(sales - credit)}</strong></div>
    <div class="summary-row"><span>Credit sales</span><strong>${money(credit)}</strong></div>
    <div class="summary-row"><span>Cost of goods sold</s
  
