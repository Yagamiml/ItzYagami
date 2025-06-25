const mineflayer = require('mineflayer');

function createBot() {
  const bot = mineflayer.createBot({
    host: 'kemaluan-vgnv.aternos.me',
    port: 25565,
    username: 'ItzYagami',
    version: '1.19.3'
  });

  bot.once('spawn', () => {
    bot.chat('/register 121111');
    setTimeout(() => {
      bot.chat('/login 121111');
    }, 2000);

    console.log('✅ Bot berhasil masuk & login');

    startSneakInterval(bot);

    setTimeout(() => {
      bot.chat('halo bang jangan ban aku ya');
      console.log('💬 Bot mengirim pesan auto-chat');
    }, 70000);

    bot.on('death', () => {
      console.log('💀 Bot mati, respawn dalam 3 detik...');
      setTimeout(() => bot.emit('respawn'), 3000);
    });

    bot.on('end', () => {
      console.log('🔌 Bot disconnect, mencoba reconnect dalam 5 detik...');
      setTimeout(createBot, 5000);
    });

    bot.on('error', (err) => {
      console.log('❌ Error:', err.message);
    });

    bot.on('chat', (username, message) => {
      if (username === bot.username) return;
      const msg = message.toLowerCase().trim();

      if (msg.includes('woi yagami')) {
        setTimeout(() => {
          bot.chat('apa kocak');
        }, 3000);
      }

      if (msg.includes('lu siapa')) {
        setTimeout(() => {
          bot.chat('gua Yagami boy orang paling berkuasa di server ini');
        }, 3000);
      }

      if (msg.includes('sugi suka siapa')) {
        const jawaban = [
          'Sugi suka zenin',
          'Sugi suka teli',
          'Sugi suka bagus'
        ];
        const randomJawaban = jawaban[Math.floor(Math.random() * jawaban.length)];
        setTimeout(() => {
          bot.chat(randomJawaban);
        }, 3000);
      }

      if (msg.includes('ngri')) {
        setTimeout(() => {
          bot.chat('iya lah');
        }, 3000);
      }

      if (msg.includes('kontol')) {
        setTimeout(() => {
          bot.chat('mulut lu kek air comberan, dijaga dikit');
        }, 3000);
      }

      if (msg.includes('ireng')) {
        setTimeout(() => {
          bot.chat('Ireng = jawa');
        }, 3000);
      }

      if (msg === 'sugi') {
        setTimeout(() => {
          bot.chat('Jawa php');
        }, 3000);
      }
    });
  });
}

function startSneakInterval(bot) {
  setInterval(() => {
    bot.setControlState('sneak', true);
    console.log('🔄 Sneak ON');
    setTimeout(() => {
      bot.setControlState('sneak', false);
      console.log('🔄 Sneak OFF');
    }, 2000);
  }, 60000);
}

createBot();
