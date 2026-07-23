# Guardião Vigia — App Nativo (APK)

Este é o app do vigia, empacotado como aplicativo Android de verdade (mesmo código do sistema, mas com acesso mais confiável à localização — necessário pro sistema de rotas e checkpoint funcionar bem).

## Como gerar o APK

1. Crie um repositório novo no GitHub (ex: `rondamaster-vigia-apk`)
2. Suba todo o conteúdo desta pasta pra esse repositório
3. Vá em **Actions** no GitHub → o workflow "Gerar APK do Vigia" roda sozinho
4. Espere terminar (uns 3-5 minutos) → baixe o arquivo em **Artifacts** → `GuardiaoVigia-APK`
5. Esse `.zip` tem dentro o `app-debug.apk` — manda esse arquivo pro celular do vigia (WhatsApp, Google Drive, etc.) e instala normal (talvez precise permitir "instalar de fontes desconhecidas" no Android)

## O que muda em relação ao site

- O painel do vigia (login, plantão, rondas, checkpoints, portaria, ocorrências, relatório) é exatamente o mesmo — mesmo código, mesmo Firebase, mesmos dados
- **O botão "Gerar PDF" do relatório comum foi desativado dentro do app** — use sempre o **"🖤 Relatório Premium"** (que já funciona por código, não por impressão do navegador)
- A localização (GPS) pede permissão na primeira vez que abrir — aceite pra tudo funcionar (plantão, ronda, checkpoint)

## Próximos passos possíveis (não fiz agora, mas dá pra evoluir depois)

- **Ícone personalizado do app** — hoje usa o ícone padrão do Capacitor
- **Localização em segundo plano de verdade** — hoje o app confere a localização enquanto está aberto na tela; se quiser que funcione com o app minimizado, dá pra adicionar um plugin nativo de localização em segundo plano (mais complexo, mas possível)
- **Publicar na Play Store** — hoje o APK é instalado direto (sideload); pra Play Store precisa de conta de desenvolvedor Google (pago) e processo de revisão
