<!DOCTYPE html><html lang="en"><head>
    <title>ATM Interface Chatbot for Kids</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.3/dist/tailwind.min.css" rel="stylesheet">
  </head>
  <body class="bg-blue-100">
    <header class="text-center py-8 mb-10 bg-yellow-500 shadow-md">
      <h1 class="text-3xl font-bold text-white">
    ATM Login
</h1>
    </header>
    <div class="flex justify-center">
      <div class="px-2 w-full max-w-2xl">
        <div id="chatbox" class="flex flex-col items-start overflow-auto h-96 mb-5"></div>
        <div class="flex flex-row justify-between p-2 bg-white shadow rounded border border-gray-200">
          <button class="bg-yellow-500 text-white font-bold py-2 px-4 rounded" id="transactionHistory">Transaction History</button>
          <button class="bg-yellow-500 text-white font-bold py-2 px-4 rounded" id="withdraw">Withdraw</button>
          <button class="bg-yellow-500 text-white font-bold py-2 px-4 rounded" id="deposit">Deposit</button>
          <button class="bg-yellow-500 text-white font-bold py-2 px-4 rounded" id="transfer">Transfer</button>
          <button class="bg-red-500 text-white font-bold py-2 px-4 rounded" id="quit">Quit</button>
        </div>
      </div>
    </div>
    <script>
      const chatbox = document.getElementById("chatbox");
      const transactionHistoryBtn = document.getElementById("transactionHistory");
      const withdrawBtn = document.getElementById("withdraw");
      const const transferBtn = document.getElementById("transfer");
      const quitBtn = document.getElementById("quit");

      function createMessageElement(text, userType) {
        const messageElement = document.createElement("div");
        messageElement.className = `inline-block my-2.5 p-2.5 rounded border ${userType === 'user' ? 'bg-blue-400 self-end' : 'bg-yellow-300 self-start'}`;
        messageElement.textContent = text;
        return messageElement;
      }

      function appendMessage(text, userType) {
        const messageElement = createMessageElement(text, userType);
        chatbox.appendChild(messageElement);
        chatbox.scrollTop = chatbox.scrollHeight;
      }

      transactionHistoryBtn.addEventListener("click", () => {
        appendMessage("Show Transaction History", "user");
        appendMessage("Transaction history displayed here.", "atm");
      });

      withdrawBtn.addEventListener("click", () => {
        appendMessage("Withdraw", "user");
        appendMessage("Enter the amount you want to withdraw.", "atm");
      });

      depositBtn.addEventListener("click", () => {
        appendMessage("Deposit", "user");
        appendMessage("Enter the amount you want to deposit.", "atm");
      });

      transferBtn.addEventListener("click", () => {
        appendMessage("Transfer", "user");
        appendMessage("Enter the account and amount to transfer the money.", "atm");
      });

      quitBtn.addEventListener("click", () => {        appendMessage("Quit", "user");
        appendMessage("Thank you for using. Goodbye!", "atm");
      });
    </script>
  
</body></html>
	
	 
      
