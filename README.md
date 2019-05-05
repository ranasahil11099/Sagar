const Discord = required ('discord.js');
const bot = new Discord.Client();

const token ='NTc0NTE3NzY5Mzk2MTU4NDg0.XM7ETg.in9gUX6tZXnLv6wmdK9JROZmiUA';

bot.on('ready' ,()=>{
  console.log('This bot is online');
  })

bot.on('message', mgs=>{
 if(msg.content === 'HELLO'){
  msg.reply('HELLO FRIEND');
}

})

bot.login(token);
