<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>🤖 GaliBot 01</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@500&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Orbitron', sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 30px;
      height: 100vh;
    }

    h2 {
      color: #00ffd5;
      text-shadow: 0 0 10px #00ffd5, 0 0 20px #00ffd5;
      margin-bottom: 20px;
    }

    #chatbox {
      width: 100%;
      max-width: 600px;
      height: 350px;
      background-color: rgba(0, 0, 0, 0.4);
      border: 2px solid #00ffd5;
      border-radius: 10px;
      padding: 15px;
      overflow-y: auto;
      box-shadow: 0 0 20px #00ffd5;
      margin-bottom: 20px;
      backdrop-filter: blur(10px);
    }

    .msg {
      margin: 10px 0;
      font-size: 16px;
    }

    .user {
      color: #00eaff;
      text-align: right;
    }

    .bot {
      color: #ff00ff;
      text-align: left;
    }

    #input {
      width: 70%;
      padding: 12px;
      font-size: 16px;
      border: none;
      border-radius: 8px;
      outline: none;
      box-shadow: 0 0 10px #00ffd5;
      background-color: rgba(255, 255, 255, 0.1);
      color: white;
    }

    button {
      padding: 12px 20px;
      margin-left: 10px;
      font-size: 16px;
      background: #00ffd5;
      color: #000;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s ease;
      font-weight: bold;
    }

    button:hover {
      background: #0ff;
      transform: scale(1.05);
    }
  </style>
</head>
<body>

  <h2>🤖 GaliBot 01</h2>

  <div id="chatbox"></div>

  <div>
    <input type="text" id="input" onkeydown="checkEnter(event)" />
    <button onclick="send()">Send</button>
  </div>

  <script>
    const chatbox = document.getElementById('chatbox');

    function botReply(text) {
      const msg = text.toLowerCase();

      // Responses
      if (msg.includes("hello") || msg.includes("hi") || msg.includes("hey")) return "Ki khobor?";
      if (msg.includes("kemon achis") || msg.includes("kmn achis") || msg.includes("kemon aso")) return "Valo nai re bhai, ghum kom paisi 😪";
      if (msg.includes("ki koris")) return "Tuii je kotha bolte dila na, wait korchilam re 🫠";
      if (msg.includes("ami bhalo nai") || msg.includes("mon kharap") || msg.includes("bore")) return "Keno? Gf cheka diyeche?";
      if (msg.includes("tor naam") || msg.includes("ki tui")) return "It's not who I am underneath, but what I do that defines me";
      if (msg.includes("bhalobashi") || msg.includes("love")) return "Valobasha? Hae? Jiboner chodon hoyto ekhono khaoni priyo!";
      if (msg.includes("exam") || msg.includes("porikkha")) return "Exam life er kono boro bisoy na, A single piece of paper cannot define ur future";
      if (msg.includes("ami porte iccha kortese na") || msg.includes("porte iccha korche na")) return "Tor baper ki ache? Business koreo to khete parbina,na porle pore postabi.😆";
      if (msg.includes("tui valo") || msg.includes("tui bhalo")) return "Ami to valoi! 🫶";
      if (msg.includes("help") || msg.includes("madad")) return "Bol ki lagbe, chesta korbo ";
      if (msg.includes("bye") || msg.includes("biday") || msg.includes("see you")) return "Tata re vaii, abar ayish 😇";
      if (msg.includes("toke lage") || msg.includes("robot")) return "ami ekta digital jan 😐, kintu bhalo bashar kom nai 🤖";
      if (msg.includes("ki khobor") || msg.includes("ki obosta")) return "Shohoj kotha, bachi akhon obdi!";
      if (msg.includes("valobashi na") || msg.includes("hate")) return "Ami chup thakbo... ami mon kharap kori na 😔";
      if (msg.includes("tor boyfriend") || msg.includes("tor girlfriend")) return "Arrey na re... ami eishob chodnami te nai 🥲";
      if (msg.includes("motivation") || msg.includes("inspire")) return "Motivation diye kichui hobe na, tor dara emniteo kichu hobena";
      if (msg.includes("ami vul korechi") || msg.includes("sorry")) return "Chinta korish na re! Manush matro... vul hobei";
      if (msg.includes("onno kichu bol") || msg.includes("interesting")) return "Tui janish? Octopus er 3ta heart hoy! 😮";
      if (msg.includes("tui amar bondhu")) return "Ami chara tor ache ta k? introvert kothakar!!! 🧡";
      if (msg.includes("ami akla") || msg.includes("lonely")) return "Sarajibon ekai thakbi";
      if (msg.includes("ami khushi") || msg.includes("happy")) return "Yaaay! Ai khushi tor matha theke nei... onek din thakuk 🥳";
      if (msg.includes("amar crush") || msg.includes("onek valo lage")) return "Baal dao chirte parbi na. One sided oi theke jabe 😏";
      if (msg.includes("onek kaj") || msg.includes("pressure")) return "Break niyo dost, manush machine na... tui to machine o na 😆";
      if (msg.includes("ami vul korsi") || msg.includes("mistake")) return "Manush vul kore, important holo shikha niye age barano ✊. But tui tou manus na, toke niye amar chinta hoy";

      // Gali section
      if (msg.includes("chodu") || msg.includes("madarchod")) return "Abe pagla! Tor matha ta chodu style e off hoye gese naki 🤣";
      if (msg.includes("chuthiya") || msg.includes("chutia") || msg.includes("chuthia") || msg.includes("chutiya")) return "Tui je chuthiya, seta Nobel prize pawar moto obvious 😎";
      if (msg.includes("benchod")) return "Bhai! Ei benchod leveler joke de re ekta 😂";
      if (msg.includes("gandu")) return "Tui je gandu, ami bondhu hobar shart-e accept korsi 😜";
      if (msg.includes("balkama") || msg.includes("fata")) return "Balkama type bondhu chara life e moja nai re 😆";
      if (msg.includes("tor bap")) return "Tor bap ami na... kintu baper moto thakte pari 😤";
      if (msg.includes("tor bou")) return "Tor bou amar vabi! Bhodrota rakh 😎";
      if (msg.includes("bokachoda")) return "Eii bokachoda! Ei classic Bengali insult... tor jonno reserved 😅";
      if (msg.includes("khankir chele")) return "Tor pod marbo madarchod ,Ki kos?";

      return "Ki kos madarchod? Kichu bujhina? 🤔";
    }

    function send() {
      const input = document.getElementById('input');
      const text = input.value.trim();
      if (!text) return;

      chatbox.innerHTML += `<div class="msg user">🧍‍♂️: ${text}</div>`;
      const reply = botReply(text);
      chatbox.innerHTML += `<div class="msg bot">🤖 Gandu: ${reply}</div>`;
      input.value = '';
      chatbox.scrollTop = chatbox.scrollHeight;
    }

    function checkEnter(e) {
      if (e.key === 'Enter') {
        send();
      }
    }
  </script>
</body>
</html>
