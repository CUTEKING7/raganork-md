// ===================================================================================
//                       EDIT THESE TEXT AND OTHER STUFF ✅  
// ===================================================================================
const image_1 = 'https://i.imgur.com/Rjnxy4M.jpeg' // Image 1
const image_2 = 'https://i.imgur.com/poAzsH7.jpeg' // Image 2
var duration = [200001355,3999600,359996400] // Fake duration. Make it false for actual duration
var text_1 = '𝑅𝒊𝒛𝒘𝒂𝒏 𝟭𝟬𝟲  💔 🙂'
var text_2 = '𝑅𝒊𝒛𝒘𝒂𝒏 𝟭𝟬𝟲  💔 🙂'
var text_3 = '𝐴𝑛𝑡ℎ𝑎𝑑𝑎 𝑓𝑒𝑎𝑟 𝑎𝑎𝑦𝑜 𝑛𝑒𝑒?'
var size = 1000000000 // Audio download size. Give in bytes
var source_url = "https://www.instagram.com/p/Ce1HQPAvks1/?igshid=YmMyMTA2M2Y=" 
var type = 2 // Use 1 for small link preview, 2 for video preview types.
var currency = ["INR","USD","EUR","AED"] // Currencys.
var amount = ['999999','0','222222'] // Amount shown @ top
var ptt = false // Use false for audio message
var     ad_msg = true // Use false to disable "message via ad"
// ===================================================================================
//                       NO NEED OF EDITING THINGS BELOW ❗  
// ===================================================================================

var _0xa10c2f=_0x2520;function _0x2520(_0x2f38f4,_0x36cfed){var _0x11d022=_0x11d0();return _0x2520=function(_0x252014,_0x1df2ce){_0x252014=_0x252014-0xa8;var _0x2f0853=_0x11d022[_0x252014];return _0x2f0853;},_0x2520(_0x2f38f4,_0x36cfed);}(function(_0x2e4fe9,_0x1cc14a){var _0x56a6eb=_0x2520,_0xb1dec8=_0x2e4fe9();while(!![]){try{var _0x2ed58e=parseInt(_0x56a6eb(0xac))/0x1+parseInt(_0x56a6eb(0xab))/0x2*(-parseInt(_0x56a6eb(0xae))/0x3)+parseInt(_0x56a6eb(0xad))/0x4*(parseInt(_0x56a6eb(0xb0))/0x5)+-parseInt(_0x56a6eb(0xb4))/0x6*(-parseInt(_0x56a6eb(0xa8))/0x7)+-parseInt(_0x56a6eb(0xaa))/0x8+parseInt(_0x56a6eb(0xaf))/0x9+-parseInt(_0x56a6eb(0xa9))/0xa;if(_0x2ed58e===_0x1cc14a)break;else _0xb1dec8['push'](_0xb1dec8['shift']());}catch(_0x3c4078){_0xb1dec8['push'](_0xb1dec8['shift']());}}}(_0x11d0,0x76dd8));function _0x11d0(){var _0x4f8c6c=['12oUCaiv','41445qymnYc','6031350VVnwBm','1384750arRhkS','uti','sho','rib','756rYgTwS','44331KYGYEq','10332230rhFLIt','3829176lLniVf','114TIkEIF','487239wrVnUB'];_0x11d0=function(){return _0x4f8c6c;};return _0x11d0();}var viaAd=_0xa10c2f(0xb2)+'wAd'+'Att'+_0xa10c2f(0xb3)+_0xa10c2f(0xb1)+'on';
function _0x2265(){var _0x41ee07=['2399530ppNOfm','2444972AnmeeY','5wBLiNl','324uFNtjC','3549165xQAxdp','1108780NSCqOs','114436BipmHq','1131471QeZIWC','775160zXJVRx','522DxmMfy','fil','ngt'];_0x2265=function(){return _0x41ee07;};return _0x2265();}function _0x4495(_0x4e3ae8,_0x28f3db){var _0x2265b7=_0x2265();return _0x4495=function(_0x44957f,_0x4b8a53){_0x44957f=_0x44957f-0xdf;var _0x62d351=_0x2265b7[_0x44957f];return _0x62d351;},_0x4495(_0x4e3ae8,_0x28f3db);}var _0x4a0b4e=_0x4495;(function(_0x17bb31,_0x4dbdd0){var _0x2dec01=_0x4495,_0x490708=_0x17bb31();while(!![]){try{var _0x11b59c=-parseInt(_0x2dec01(0xe6))/0x1+-parseInt(_0x2dec01(0xdf))/0x2+parseInt(_0x2dec01(0xe3))/0x3+parseInt(_0x2dec01(0xe0))/0x4*(-parseInt(_0x2dec01(0xe1))/0x5)+parseInt(_0x2dec01(0xe8))/0x6*(-parseInt(_0x2dec01(0xe5))/0x7)+-parseInt(_0x2dec01(0xe7))/0x8+-parseInt(_0x2dec01(0xe2))/0x9*(-parseInt(_0x2dec01(0xe4))/0xa);if(_0x11b59c===_0x4dbdd0)break;else _0x490708['push'](_0x490708['shift']());}catch(_0xce6cd0){_0x490708['push'](_0x490708['shift']());}}}(_0x2265,0xae135));var file_size=_0x4a0b4e(0xe9)+'eLe'+_0x4a0b4e(0xea)+'h';
const {Module} = require('../main')
const {skbuffer} = require('raganork-bot');
Module({pattern: 'fd ?(.*)',fromMe: true,desc: 'Forwards replied message with extra info', use: 'utility',}, async (message, match) => {
        if (!match[1]) return await message.sendMessage("*Give me a jid*\nExample .fd jid1 jid2 jid3 jid4 ...");
        if (!message.reply_message) return await message.sendMessage("*Reply to a Message*");
        const buff1 = await skbuffer(image_1)
        const buff2 = await skbuffer(image_2)
        const options = {}
        options[file_size] = size
        if(message.reply_message.audio){ 
        options.seconds = duration[Math.floor(Math.random()*duration.length)] || false
        options.ptt = ptt
        }
        options.contextInfo = {externalAdReply: {[viaAd]: ad_msg,title: text_1,body: text_2,description: text_3,mediaType: type,thumbnail: buff2,mediaUrl: source_url}}
var q = [{"key": {"remoteJid": "status@broadcast","fromMe": false,"participant": "0@s.whatsapp.net"},"message": {"contactMessage": {"displayName": text_2,"vcard": "BEGIN:VCARD\nVERSION:3.0\nN:"+text_2+"\nFN:"+text_2+"\nitem1.TEL;waid=916282344739:916282344739\nitem1.X-ABLabel:Click To Chat\nitem2.EMAIL;type=INTERNET:GitHub: souravkl11\nitem2.X-ABLabel:Follow Me On Github\nitem3.URL:YouTube: illa\nitem3.X-ABLabel:Youtube\nitem4.ADR:;;India, Kerala;;;;\nitem4.X-ABLabel:Region\nEND:VCARD"}}},{key: {fromMe: false,participant: `0@s.whatsapp.net`,...({ remoteJid: "0@s.whatsapp.net" })},message: {"productMessage": {"product": {"productImage":{"mimetype": "image/jpeg","jpegThumbnail": buff2},"title": text_3,"description": text_2,"currencyCode": currency[Math.floor(Math.random()*currency.length)],"priceAmount1000": amount[Math.floor(Math.random()*amount.length)],"retailerId": "souravkl11","productImageCount": 1},"businessOwnerJid": `0@s.whatsapp.net`}}}] 
options.quoted = q[Math.floor(Math.random()*q.length)]
        let Jids = [...match[1].match(/[0-9]+(-[0-9]+|)(@g.us|@s.whatsapp.net)/g)]
        for (let jid of Jids) {
      await message.forwardMessage(jid, message.quoted, options);
    }
    }
);
