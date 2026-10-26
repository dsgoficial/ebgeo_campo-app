# EBGeo Campo: o app para baixar

Este repositório só publica o app Android do EBGeo Campo: as versões em [Releases](https://github.com/dsgoficial/ebgeo_campo-app/releases) e a página de download em https://dsgoficial.github.io/ebgeo_campo-app/ (GitHub Pages, desta pasta). O código é do repositório privado 1cgeo/ebgeo_campo, e a publicação segue `ferramentas/publicar/` de lá.

## Versões

- A versão segue `MAIOR.MENOR.CORREÇÃO`, e o release se chama `v` mais ela (`v0.2.0`). A mesma versão está no app (`VERSAO_APP`, que ele mostra e manda ao EBGeo) e no `versionName` do Android; o `versionCode` só cresce, e o Android recusa instalar por cima um número menor.
- Cada release traz o mesmo APK com dois nomes: `ebgeo-campo.apk`, sempre igual, para o link fixo `releases/latest/download/ebgeo-campo.apk`, e `ebgeo-campo-<versão>.apk`, que o botão da página baixa, para o celular não confundir o download novo com o velho (desde a 0.1.5). As notas trazem o que mudou, numa linha por item, e no fim o SHA-256 do APK e o do certificado que o assina. A página lista as dez últimas versões com as notas.
- Versão publicada não se apaga nem se troca: o conserto sai como versão nova. Quando a velha tiver de parar, o EBGeo sobe `CAMPO_VERSAO_MINIMA_APP`, e o app abaixo dela recebe "atualize o app" com o endereço desta página.

## O certificado

O certificado é o mesmo em todas as versões: o Android só instala por cima o APK assinado pela mesma chave, e o EBGeo recusa o app com outra assinatura (`CAMPO_ASSINATURAS_APK`). A impressão digital SHA-256 dele está na página e em `ferramentas/publicar/certificado.sha256` do repositório do código, e o script de publicação recusa o APK assinado por outra chave.
