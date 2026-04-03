<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SARKAR PANEL | OFFICIAL</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        body { background-color: #0b0f1a; font-family: 'Segoe UI', sans-serif; color: white; overflow-x: hidden; }
        .glass-card { background: rgba(23, 32, 51, 0.8); backdrop-filter: blur(15px); border: 1px solid rgba(59, 130, 246, 0.2); }
        .animate-scan { position: relative; overflow: hidden; }
        .animate-scan::after { content: ""; position: absolute; top: 0; left: 0; width: 100%; height: 4px; background: #3b82f6; animation: scan 2s linear infinite; box-shadow: 0 0 15px #3b82f6; }
        @keyframes scan { 0% { top: 0; } 100% { top: 100%; } }
        .success-check { font-size: 80px; color: #22c55e; animation: scaleUp 0.5s ease-out; }
        @keyframes scaleUp { 0% { transform: scale(0); } 100% { transform: scale(1); } }
    </style>
</head>
<body class="flex flex-col items-center justify-center min-h-screen p-4">

    <div id="mainPanel" class="w-full max-w-sm glass-card rounded-3xl p-6 shadow-2xl text-center">
        <h1 class="text-2xl font-black text-blue-500 mb-2 italic">SARKAR PANEL 👑</h1>
        <p class="text-gray-400 text-xs mb-6 uppercase tracking-widest">Official Merchant Account</p>

        <div class="bg-white p-4 rounded-2xl mb-4 inline-block animate-scan">
            <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=upi://pay?pa=akash3729@fam&pn=Sarkar%20Panel&am=500&cu=INR" alt="QR Code" class="w-40 h-40">
        </div>
        
        <div class="bg-blue-900/30 p-4 rounded-xl border border-blue-500/20 mb-6">
            <p class="text-gray-400 text-sm">Payable Amount</p>
            <p class="text-3xl font-bold text-white">₹500.00</p>
        </div>

        <button onclick="startPayment()" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-bold py-4 rounded-2xl transition-all active:scale-95 shadow-lg shadow-blue-600/30">
            CONFIRM PAYMENT
        </button>
        
        <button onclick="openAdmin()" class="mt-4 text-xs text-gray-500 hover:text-blue-400">Admin Login</button>
    </div>

    <div id="processing" class="hidden fixed inset-0 bg-slate-950 flex flex-col items-center justify-center z-50">
        <div class="w-16 h-16 border-4 border-blue-500 border-t-transparent rounded-full animate-spin mb-4"></div>
        <p class="text-xl font-medium">Verifying Transaction...</p>
        <p class="text-gray-400 text-sm mt-2">Checking with UPI Server</p>
    </div>

    <div id="success" class="hidden fixed inset-0 bg-slate-950 flex flex-col items-center justify-center z-50 text-center p-6">
        <i class="fas fa-check-circle success-check mb-4"></i>
        <h2 class="text-3xl font-bold mb-2">Payment Received!</h2>
        <p class="text-gray-400 mb-6">Transaction ID: TXN992837482</p>
        <button onclick="location.reload()" class="bg-green-600 px-8 py-3 rounded-full font-bold">Done</button>
    </div>

    <div id="adminModal" class="hidden fixed inset-0 bg-black/90 flex items-center justify-center p-6 z-50">
        <div class="glass-card w-full max-w-xs p-6 rounded-2xl text-center">
            <h3 class="text-lg font-bold mb-4">Secure Admin Access</h3>
            <input type="password" id="pinInput" placeholder="Enter PIN" class="w-full bg-slate-900 border border-slate-700 p-3 rounded-xl mb-4 text-center">
            <div class="flex gap-2">
                <button onclick="closeAdmin()" class="w-1/2 bg-slate-800 py-2 rounded-xl">Cancel</button>
                <button onclick="verifyPin()" class="w-1/2 bg-blue-600 py-2 rounded-xl">Login</button>
            </div>
        </div>
    </div>

    <script>
        function startPayment() {
            document.getElementById('processing').classList.remove('hidden');
            setTimeout(() => {
                document.getElementById('processing').classList.add('hidden');
                document.getElementById('success').classList.remove('hidden');
            }, 4000); // 4 Second processing time
        }

        function openAdmin() { document.getElementById('adminModal').classList.remove('hidden'); }
        function closeAdmin() { document.getElementById('adminModal').classList.add('hidden'); }

        function verifyPin() {
            if(document.getElementById('pinInput').value === '3729') {
                alert("Welcome Admin! Access Granted.");
                window.location.reload();
            } else {
                alert("Wrong PIN!");
            }
        }
    </script>
</body>
</html>
