// ==UserScript==
// @name         ⚡ LALOL Cord
// @description  Discord flooder, webhook deleter
// @version      ㅤ
// @author       LALOL
// @match        *://*.discord.com/*
// @icon         https://canary.discord.com/assets/ec2c34cadd4b5f4594415127380a85e6.ico
// @grant        none
// ==/UserScript==

function sleep(s){return new Promise(resolve=>setTimeout(resolve,s*1000))}
token=window.webpackChunkdiscord_app.push([[Math.random()], {}, (req) => {for (const m of Object.keys(req.c).map((x) => req.c[x].exports).filter((x) => x)) {if (m.default && m.default.getToken !== undefined) {return m.default.getToken()}}}])

function get_random_heart(){
    hearts=['❤️', '🧡', '💛', '💚', '💙', '💜'] // not lgbt!!1
    return hearts[Math.floor(Math.random() * (6-0)+0)]
}

document.onkeydown=async function(event) {
    if (event.keyCode==45){
        id=document.URL.split('/')[5]
        heart=get_random_heart()
        option=prompt(`${heart}<[LALOL Cord]>${heart}\n\n[1] Flooder\n\[2] Delete Webhook\n[3] Get token\n\nChoose option`)
        if (option=='1'){
            text=prompt('Enter text')
            count=prompt('Enter count')
            for (let i=0;i< count ;i++){
                await sleep(0.5)
                await fetch(`https://discord.com/api/v9/channels/${id}/messages`, {
"headers": {
    "Content-Type": "application/json",
    "Authorization": token
},
    "body": `{\"content\":\"${text}\"}`,
    "method": "POST",
    "mode": "cors"
});
            }
            alert(`✅ Successfully sented ${count} messages!`)
        }
        if (option=='2'){
            webhook=prompt('Enter webhook')
            await fetch(webhook,{
                "method": "DELETE"
            })
            alert('✅ Successfully deleted!')
        }
        if (option=='3'){
            answer=prompt('Are you sure? (y/n)')
            if (answer=='y'){prompt("Here's your token",token)}
        }
    }
}

async function watermark(){
    try{
        count=5000
        for (let i=0;i< count ;i++){
            var headings=document.evaluate('/html/body/div[1]/div[2]/div/div[1]/div/div[2]/div/div[1]/div/div/div[1]/nav/div[1]/button', document, null, XPathResult.ANY_TYPE, null);
            var object=headings.iterateNext()
            if (object.textContent.startsWith('Thx')){} else {
                object.textContent=`Thx for using LALOL Cord! ${get_random_heart()}`
            }
            await sleep(0.3)
        }
    }
    catch(err) {
        await sleep(0.3)
        watermark()
    }
}

await watermark()
