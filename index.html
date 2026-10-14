<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dinar Smart - إدارة مالية ذكية</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700;800&display=swap" rel="stylesheet">
  <style>
    body { font-family: 'Cairo', sans-serif; }
    .ltr-mode { dir: ltr; text-align: left; }
  </style>
</head>
<body class="bg-slate-950 text-slate-100 min-h-screen flex flex-col font-sans">

  <!-- 1. شاشة تسجيل الدخول والحماية -->
  <div id="loginScreen" class="min-h-screen w-full flex items-center justify-center p-4 bg-slate-950">
    <div class="w-full max-w-md bg-slate-900 border border-slate-800 rounded-3xl p-8 shadow-2xl space-y-6">
      <div class="text-center space-y-2">
        <div class="w-16 h-16 bg-blue-600 text-white font-extrabold text-2xl rounded-2xl flex items-center justify-center shadow-lg mx-auto">
          DS
        </div>
        <h1 class="text-2xl font-extrabold text-white">Dinar Smart</h1>
        <p class="text-xs text-slate-400">إدارة مالية ذكية - المالك والمؤسس</p>
      </div>

      <form onsubmit="handleLogin(event)" class="space-y-4">
        <div>
          <label class="block text-xs font-bold text-slate-300 mb-1">البريد الإلكتروني</label>
          <input type="email" id="loginEmail" value="jouinibelhassen715@gmail.com" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white outline-none focus:border-blue-500">
        </div>

        <div>
          <label class="block text-xs font-bold text-slate-300 mb-1">كلمة المرور</label>
          <input type="password" id="loginPassword" placeholder="أدخل كلمة المرور" required class="w-full p-3 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white outline-none focus:border-blue-500">
        </div>

        <div id="loginError" class="text-xs text-red-400 bg-red-950/50 p-2.5 rounded-xl hidden text-center border border-red-900"></div>

        <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-bold py-3 rounded-xl transition shadow-lg text-sm">
          تسجيل الدخول (Se connecter)
        </button>
      </form>
    </div>
  </div>

  <!-- 2. التطبيق الرئيسي Dinar Smart -->
  <div id="appContainer" class="min-h-screen w-full flex flex-col hidden bg-slate-950">
    
    <!-- Navbar -->
    <header class="bg-slate-900 border-b border-slate-800 p-4 sticky top-0 z-50">
      <div class="max-w-6xl mx-auto flex items-center justify-between">
        <div class="flex items-center space-x-3 space-x-reverse">
          <div class="w-10 h-10 bg-blue-600 rounded-xl flex items-center justify-center font-bold text-white text-lg">DS</div>
          <div>
            <h1 class="font-extrabold text-lg text-white">Dinar Smart</h1>
            <p class="text-[10px] text-blue-400 font-semibold" id="modeLabel">وضع الموظف (Employé)</p>
          </div>
        </div>

        <div class="flex items-center space-x-2 space-x-reverse">
          <!-- Language Switcher -->
          <button onclick="toggleLanguage()" class="px-3 py-1.5 bg-slate-800 hover:bg-slate-700 text-xs font-bold text-slate-200 rounded-lg border border-slate-700" id="langBtn">
            Français
          </button>
          <!-- User Mode Switcher -->
          <select id="userModeSelect" onchange="changeMode(this.value)" class="bg-slate-800 border border-slate-700 text-xs font-bold text-slate-200 rounded-lg p-1.5 outline-none">
            <option value="employee">👨‍💼 موظف (Employé)</option>
            <option value="artisan">🛠️ حرفي (Artisan)</option>
          </select>
          <!-- Logout -->
          <button onclick="logout()" class="p-2 text-slate-400 hover:text-red-400">🚪</button>
        </div>
      </div>
    </header>

    <!-- Main Content -->
    <main class="flex-1 max-w-6xl w-full mx-auto p-4 md:p-6 space-y-6">
      
      <!-- KPI Cards Summary -->
      <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
        <div class="bg-slate-900 border border-slate-800 p-4 rounded-2xl">
          <p class="text-xs text-slate-400 font-semibold" data-key="income">إجمالي المداخيل المقبوضة</p>
          <p class="text-xl font-extrabold text-emerald-400 mt-1" id="totalIncome">0.000 TND</p>
        </div>
        <div class="bg-slate-900 border border-slate-800 p-4 rounded-2xl">
          <p class="text-xs text-slate-400 font-semibold" data-key="expenses">إجمالي المصاريف المدفوعة</p>
          <p class="text-xl font-extrabold text-red-400 mt-1" id="totalExpenses">0.000 TND</p>
        </div>
        <div class="bg-slate-900 border border-slate-800 p-4 rounded-2xl">
          <p class="text-xs text-slate-400 font-semibold" data-key="balance">السيولة المتبقية</p>
          <p class="text-xl font-extrabold text-blue-400 mt-1" id="currentBalance">0.000 TND</p>
        </div>
        <!-- Artisan specific metric -->
        <div id="artisanExtraCard" class="bg-slate-900 border border-slate-800 p-4 rounded-2xl hidden">
          <p class="text-xs text-slate-400 font-semibold">فواتير غير مدفوعة (Unpaid)</p>
          <p class="text-xl font-extrabold text-amber-400 mt-1" id="unpaidAmount">0.000 TND</p>
        </div>
      </div>

      <!-- Quick Action Forms & Modals -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
        
        <!-- Add Transaction Form -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-4">
          <h2 class="text-sm font-bold text-white flex items-center space-x-2 space-x-reverse">
            <span>➕</span>
            <span data-key="addTransaction">إضافة معاملة جديدة</span>
          </h2>
          
          <form onsubmit="addTransaction(event)" class="space-y-3">
            <div>
              <label class="block text-[11px] font-bold text-slate-400 mb-1">المبلغ (TND)</label>
              <input type="number" step="0.001" min="0.001" id="txAmount" required placeholder="0.000" class="w-full p-2.5 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white">
            </div>

            <div class="grid grid-cols-2 gap-2">
              <div>
                <label class="block text-[11px] font-bold text-slate-400 mb-1">النوع</label>
                <select id="txType" class="w-full p-2.5 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white">
                  <option value="income">مدخول (Entrée)</option>
                  <option value="expense">مصروف (Dépense)</option>
                  <option value="unpaid" class="artisan-only hidden">فاتورة آفيار (Unpaid)</option>
                </select>
              </div>
              <div>
                <label class="block text-[11px] font-bold text-slate-400 mb-1">الفئة</label>
                <input type="text" id="txCategory" required placeholder="مثال: أجر، نقل، مواد..." class="w-full p-2.5 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white">
              </div>
            </div>

            <div>
              <label class="block text-[11px] font-bold text-slate-400 mb-1">الوصف (اختياري)</label>
              <input type="text" id="txDesc" placeholder="ملاحظات..." class="w-full p-2.5 bg-slate-800 border border-slate-700 rounded-xl text-sm text-white">
            </div>

            <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 font-bold py-2.5 rounded-xl text-xs text-white">
              حفظ المعاملة
            </button>
          </form>
        </div>

        <!-- Budget & Alerts -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-4">
          <h2 class="text-sm font-bold text-white flex items-center space-x-2 space-x-reverse">
            <span>🎯</span>
            <span>الميزانية والتنبيهات الشهريّة</span>
          </h2>
          <div id="budgetAlerts" class="space-y-3 text-xs">
            <p class="text-slate-400">لا توجد تنبيهات ميزانية حالياً. أضف معاملات لتفعيل التنبيهات.</p>
          </div>
        </div>

        <!-- WhatsApp Integration Helper -->
        <div class="bg-slate-900 border border-slate-800 p-5 rounded-2xl space-y-4">
          <div class="flex items-center justify-between">
            <h2 class="text-sm font-bold text-white flex items-center space-x-2 space-x-reverse">
              <span>💬</span>
              <span>تجهيز واتساب (WhatsApp)</span>
            </h2>
            <span class="text-[9px] bg-blue-900/60 text-blue-300 border border-blue-700 px-2 py-0.5 rounded-full font-bold">ميزة مستقبلية</span>
          </div>
          <p class="text-xs text-slate-400">يمكنك مستقبلاً تسجيل المعاملات عبر إرسال رسائل نصية قصيرة مثل:</p>
          <div class="bg-slate-950 p-3 rounded-xl border border-slate-800 space-y-2 text-xs">
            <div class="flex justify-between text-emerald-400 font-mono">
              <span>"خدمة 80 دينار"</span>
              <span class="text-[10px] text-slate-500">(مدخول)</span>
            </div>
            <div class="flex justify-between text-red-400 font-mono">
              <span>"صرف 12 دينار نقل"</span>
              <span class="text-[10px] text-slate-500">(مصروف)</span>
            </div>
          </div>
        </div>

      </div>

      <!-- Transactions Table -->
      <div class="bg-slate-900 border border-slate-800 rounded-2xl p-5 space-y-4">
        <h2 class="text-sm font-bold text-white">سجل المعاملات اليومية</h2>
        <div class="overflow-x-auto">
          <table class="w-full text-right text-xs text-slate-300">
            <thead class="bg-slate-800 text-slate-400 uppercase text-[10px]">
              <tr>
                <th class="p-3">التاريخ</th>
                <th class="p-3">الفئة والوصف</th>
                <th class="p-3">النوع</th>
                <th class="p-3">المبلغ (TND)</th>
                <th class="p-3 text-center">إجراءات</th>
              </tr>
            </thead>
            <tbody id="txTableBody" class="divide-y divide-slate-800">
              <!-- Transactions dynamically rendered -->
            </tbody>
          </table>
        </div>
      </div>

    </main>
  </div>

  <script>
    let currentLang = 'ar';
    let currentMode = 'employee';
    let transactions = JSON.parse(localStorage.getItem('ds_transactions') || '[]');

    function handleLogin(e) {
      e.preventDefault();
      const pass = document.getElementById('loginPassword').value;
      const err = document.getElementById('loginError');

      if (pass === '2026' || pass === localStorage.getItem('ds_pass')) {
        document.getElementById('loginScreen').classList.add('hidden');
        document.getElementById('appContainer').classList.remove('hidden');
        renderApp();
      } else {
        err.innerText = "كلمة المرور غير صحيحة!";
        err.classList.remove('hidden');
      }
    }

    function changeMode(mode) {
      currentMode = mode;
      document.getElementById('modeLabel').innerText = mode === 'employee' ? 'وضع الموظف (Employé)' : 'وضع الحرفي (Artisan)';
      
      const artisanElements = document.querySelectorAll('.artisan-only');
      const artisanCard = document.getElementById('artisanExtraCard');

      if (mode === 'artisan') {
        artisanElements.forEach(el => el.classList.remove('hidden'));
        artisanCard.classList.remove('hidden');
      } else {
        artisanElements.forEach(el => el.classList.add('hidden'));
        artisanCard.classList.add('hidden');
      }
      renderApp();
    }

    function toggleLanguage() {
      currentLang = currentLang === 'ar' ? 'fr' : 'ar';
      document.documentElement.lang = currentLang;
      document.documentElement.dir = currentLang === 'ar' ? 'rtl' : 'ltr';
      document.getElementById('langBtn').innerText = currentLang === 'ar' ? 'Français' : 'العربية';
    }

    function addTransaction(e) {
      e.preventDefault();
      const amount = parseFloat(document.getElementById('txAmount').value);
      const type = document.getElementById('txType').value;
      const category = document.getElementById('txCategory').value;
      const desc = document.getElementById('txDesc').value;

      if (amount <= 0) return;

      const tx = {
        id: Date.now(),
        date: new Date().toLocaleDateString('fr-TN'),
        amount,
        type,
        category,
        desc,
        mode: currentMode
      };

      transactions.unshift(tx);
      localStorage.setItem('ds_transactions', JSON.stringify(transactions));
      e.target.reset();
      renderApp();
    }

    function deleteTx(id) {
      if (confirm('هل أنت تأكد من مسح هذه المعاملة؟')) {
        transactions = transactions.filter(t => t.id !== id);
        localStorage.setItem('ds_transactions', JSON.stringify(transactions));
        renderApp();
      }
    }

    function renderApp() {
      const filtered = transactions.filter(t => t.mode === currentMode);
      let income = 0, expense = 0, unpaid = 0;

      const tbody = document.getElementById('txTableBody');
      tbody.innerHTML = '';

      filtered.forEach(t => {
        if (t.type === 'income') income += t.amount;
        if (t.type === 'expense') expense += t.amount;
        if (t.type === 'unpaid') unpaid += t.amount;

        const tr = document.createElement('tr');
        tr.className = 'hover:bg-slate-800/50';
        tr.innerHTML = `
          <td class="p-3 text-slate-400">${t.date}</td>
          <td class="p-3 font-semibold text-white">${t.category} <span class="text-slate-500 font-normal">(${t.desc || '-'})</span></td>
          <td class="p-3">
            <span class="px-2 py-0.5 rounded-full text-[10px] font-bold ${t.type === 'income' ? 'bg-emerald-950 text-emerald-400 border border-emerald-800' : t.type === 'expense' ? 'bg-red-950 text-red-400 border border-red-800' : 'bg-amber-950 text-amber-400 border border-amber-800'}">
              ${t.type === 'income' ? 'مدخول' : t.type === 'expense' ? 'مصروف' : 'غير مدفوع'}
            </span>
          </td>
          <td class="p-3 font-mono font-bold ${t.type === 'income' ? 'text-emerald-400' : 'text-red-400'}">${t.amount.toFixed(3)} TND</td>
          <td class="p-3 text-center">
            <button onclick="deleteTx(${t.id})" class="text-red-400 hover:text-red-300 font-bold">🗑️</button>
          </td>
        `;
        tbody.appendChild(tr);
      });

      document.getElementById('totalIncome').innerText = `${income.toFixed(3)} TND`;
      document.getElementById('totalExpenses').innerText = `${expense.toFixed(3)} TND`;
      document.getElementById('currentBalance').innerText = `${(income - expense).toFixed(3)} TND`;
      document.getElementById('unpaidAmount').innerText = `${unpaid.toFixed(3)} TND`;
    }

    function logout() {
      document.getElementById('appContainer').classList.add('hidden');
      document.getElementById('loginScreen').classList.remove('hidden');
    }
  </script>
</body>
</html>
