const { setLydia, bot } = require('../lib/')

bot({
  pattern: 'lydia ?(.*)',
  desc: 'To turn on/off chat bot for all contacts',
  type: 'misc',
},
async (message, match) => {
  if (!match) return await message.send('*Example : lydia on | off*')

  const isOn = match.toLowerCase() === 'on'
  await setLydia(message.jid, isOn, null, message.id)
  await message.send(`_Lydia ${isOn ? 'Activated' : 'Deactivated'} for all contacts._`)
})
