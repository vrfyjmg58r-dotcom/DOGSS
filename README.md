# DOGSS
Painel ss

const DOGSS_URL = "https://raw.githubusercontent.com/souzaalfa/Scannerios/refs/heads/main/SOUZA_SS.js"

let req = new Request(DOGSS_URL)
let code = await req.loadString()

if (!code || code.startsWith("404")) {
  let a = new Alert()
  a.title = "DOGSS"
  a.message = "Não foi possível carregar o script."
  a.addAction("OK")
  await a.present()
} else {
  // 🔴 TROCA PRINCIPAL: Todas as variações de SOUZAASS, XUXU e similares → DOGSS
  code = code.replace(/SOUZAASS/g, "DOGSS")
  code = code.replace(/SOUZA ASS/g, "DOGSS")
  code = code.replace(/SOUZA-ASS/g, "DOGSS")
  
  // 🔴 Padrões quebrados e erros de digitação comuns
  code = code.replace(/S.*O.*U.*Z.*A.*A.*S.*S/g, "DOGSS")
  code = code.replace(/SOWZAASS/g, "DOGSS")
  code = code.replace(/SOUZAAS/g, "DOGSS")

  // 🔴 Outras variações do nome antigo
  code = code.replace(/SOUZA SS/g, "DOGSS")
  code = code.replace(/SOUZA_SS/g, "DOGSS")
  code = code.replace(/Scannerios/g, "DOGSS")
  code = code.replace(/Scanner/g, "DOGSS")
  code = code.replace(/SCANNER IOS/g, "DOGSS IOS")
  
  // 🔴 Todas as referências ao nome XUXU
  code = code.replace(/XUXU SCREENSHARE/g, "DOGSS")
  code = code.replace(/Xuxu ScreenShare/g, "DOGSS")
  code = code.replace(/XUXU SS/g, "DOGSS")
  code = code.replace(/XUXU/g, "DOGSS")

  // 🔴 Textos e cabeçalhos
  code = code.replace(/XUXU SCREENSHARE IOS/g, "DOGSS IOS")
  code = code.replace(/.*SCREENSHARE.*/g, "DOGSS IOS")

  eval(code)
}











DETECTA TUDO 