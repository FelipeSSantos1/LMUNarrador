# Narrador LMU

Narração ao vivo de corridas do **Le Mans Ultimate (LMU)** com duas vozes: um **narrador**, que descreve a ação, e um **comentarista**, que analisa a corrida. Feito para lives e gravações: o áudio sai separado, e você o capta no OBS com o VB-Cable.

Aqui estão os downloads do app e o passo a passo para **ativar a sua assinatura** e **configurar as chaves** dos serviços de IA.

- Baixe a versão mais recente em **[Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest)**.
- Assinatura (mensal ou anual): **[comprar a licença](https://lmunarrador.lemonsqueezy.com/checkout/buy/155ebdd4-f062-41fd-bb33-2cd4cab0ad5d?enabled=2305538%2C2305551)**.

---

## Sumário

1. [Instalação](#1-instalação)
2. [Ativar a sua assinatura](#2-ativar-a-sua-assinatura)
3. [Chaves de API: o que são e onde colar](#3-chaves-de-api-o-que-são-e-onde-colar)
4. [Criar a chave do Gemini](#4-criar-a-chave-do-gemini)
5. [Criar a chave do DeepSeek](#5-criar-a-chave-do-deepseek)
6. [Voz de emoção (opcional): ElevenLabs](#6-voz-de-emoção-opcional-elevenlabs)
7. [Atualizar o app](#7-atualizar-o-app)
8. [Problemas comuns](#8-problemas-comuns)
9. [Privacidade](#9-privacidade)

---

## 1. Instalação

O app é **portátil**: uma pasta, sem instalador. Para desinstalar, apague a pasta.

1. Em [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest), baixe o arquivo `NarradorLMU-<versão>-win64.zip`.
2. **Extraia** o `.zip` para uma pasta sua, por exemplo `D:\Apps\NarradorLMU`. Use sempre a mesma pasta: as suas chaves, a licença e as configurações ficam dentro dela.
3. **Ative o plugin no LMU:** *Settings → Gameplay → Enable Plugins → ON*. Depois **feche e abra o jogo por completo**. Sem isso o app fica em "LMU: aguardando o jogo".
4. Abra o LMU e o `NarradorLMU.exe` com o **mesmo nível de permissão**: os dois normais (recomendado) ou os dois como administrador. Misturar faz a leitura falhar sem mensagem de erro.
5. Dê dois cliques em `NarradorLMU.exe`.

**Aviso do Windows:** o `.exe` não tem assinatura digital de empresa. O Windows Defender ou o SmartScreen pode mostrar um aviso na primeira vez ("O Windows protegeu o computador"). Se você baixou do link oficial acima, clique em **Mais informações → Executar assim mesmo**.

**Áudio:** o app usa vozes locais (Piper e Kokoro) que já vêm na pasta. Para mandar a narração ao OBS como fonte separada, instale o [VB-Cable](https://vb-audio.com/Cable/) e escolha o dispositivo de saída na aba **Geral**.

---

## 2. Ativar a sua assinatura

**Sem licença o app abre e narra, mas só com falas prontas (templates).** Ele não usa a IA (Gemini ou DeepSeek) nem a voz de emoção. As vozes locais continuam funcionando. Com a licença ativa, a IA e a voz de emoção ficam liberadas.

### Passo a passo

1. **Compre a assinatura** pelo link: **[comprar a licença](https://lmunarrador.lemonsqueezy.com/checkout/buy/155ebdd4-f062-41fd-bb33-2cd4cab0ad5d?enabled=2305538%2C2305551)**. Você escolhe o plano mensal ou o anual. A cobrança é feita pelo Lemon Squeezy.
2. **Procure a chave de licença no e-mail** que você usou na compra. Ela também fica na sua página de pedidos do Lemon Squeezy ("Minhas compras").
3. No app, abra a aba **Licença**.
4. **Cole a chave** no campo (ele aparece mascarado) e clique em **Ativar**.
5. A aba passa a mostrar **"Licença ativa neste computador"**. A IA e a voz de emoção que você configurou voltam a funcionar a partir da próxima fala, sem reiniciar o app.

> Para a IA narrar de verdade você ainda precisa colocar a sua própria chave do Gemini ou do DeepSeek (seções 3 a 5).

### Regras da licença

- **Um computador ativo por chave.** Para usar em outro PC, abra o app no primeiro e clique em **Desativar este computador** (precisa de internet). Depois ative a mesma chave no outro PC. Se o primeiro PC não existe mais (formatou, quebrou), fale com o suporte para liberar a vaga.
- **Colar de novo a chave que já está ativa** só avisa que ela já está ativa neste computador. Colar **outra** chave troca a licença, e a anterior é desativada deste computador.
- **Quando a assinatura termina** (cancelada ou vencida), a aba mostra **"vencida"** e o app volta a narrar só com templates a partir da próxima fala. Uma linha de aviso aparece também na janela principal. Para voltar, renove em **Minhas compras** ou assine de novo pelo botão **Renovar/Assinar** da aba. Uma assinatura nova pode gerar uma chave nova: ative-a na aba.
- **Sem internet:** o app confere a licença a cada 6 horas e **aguenta até 7 dias** sem conseguir conferir. Depois disso ele mostra "Licença não confirmada" até voltar a ter internet, e então volta sozinho em alguns minutos.
- **Relógio do Windows:** voltar o relógio do computador invalida a licença até a próxima conferência online. Mantenha a hora automática ligada.
- O arquivo `licenca.dat`, na pasta do app, guarda o estado da licença. Ele fica preso ao seu computador. **Não edite, não copie para outro PC e não compartilhe**: ele contém a sua chave.

---

## 3. Chaves de API: o que são e onde colar

O app usa serviços de IA de terceiros para escrever as falas e, se você quiser, para a voz de emoção. Cada serviço exige uma **chave de API pessoal**: uma senha que identifica a sua conta, **criada por você**. O uso é cobrado (ou consome a cota gratuita) **na sua conta**, não na minha.

| Para quê | Serviço | Obrigatório? |
|---|---|---|
| Escrever as falas (a "IA") | **Gemini** (Google) **ou** DeepSeek | Você precisa de **um dos dois** |
| Voz de emoção | **ElevenLabs** (ou o Gemini TTS, com a mesma chave do Gemini) | Opcional |

**Onde colar:** aba **Chaves** do app. Há um bloco para cada serviço: cole a chave no campo e clique em **Salvar chaves**. O app mostra só os 4 últimos caracteres depois de salvar. As chaves ficam guardadas **só no seu computador**, no arquivo `chaves.toml`, dentro da pasta do app.

Regras de segurança:

- **Nunca compartilhe** uma chave de API nem o arquivo `chaves.toml`. Quem tem a chave gasta a sua conta.
- Se uma chave vazar, **apague-a no site do serviço** e crie outra.
- Prefira definir um **limite de gasto** na conta do serviço quando ele oferecer essa opção.

Os preços e as cotas gratuitas mudam com frequência: confira sempre no site de cada serviço.

---

## 4. Criar a chave do Gemini

O Gemini é o serviço de IA do Google. A chave é gerada no **Google AI Studio**.

1. Entre em **<https://aistudio.google.com/apikey>** com a sua conta Google.
2. Clique em **Create API key** (criar chave de API). Se pedir, escolha ou crie um projeto.
3. **Copie** a chave (ela começa com `AIza…`).
4. No app, aba **Chaves**, bloco **Gemini**: cole e clique em **Salvar chaves**.
5. Na aba **LLM**, escolha **Gemini**.

Documentação do Google sobre a chave: <https://ai.google.dev/gemini-api/docs/api-key>.
Preços e limites: <https://ai.google.dev/gemini-api/docs/pricing>.

A mesma chave do Gemini também serve para a **voz de emoção do Gemini TTS** (seção 6).

---

## 5. Criar a chave do DeepSeek

O DeepSeek é uma alternativa ao Gemini para escrever as falas.

1. Crie uma conta em **<https://platform.deepseek.com>** e entre.
2. Abra a página de chaves: **<https://platform.deepseek.com/api_keys>**.
3. Clique em **Create new API key**, dê um nome (por exemplo "Narrador LMU") e **copie a chave na hora**: depois de criada ela **não é mostrada de novo**.
4. O DeepSeek costuma exigir **saldo na conta** (recarga pré-paga) para a chave funcionar. Se o app disser que a chave foi recusada ou que não há saldo, confira a página de cobrança da sua conta.
5. No app, aba **Chaves**, bloco **DeepSeek**: cole e clique em **Salvar chaves**.
6. Na aba **LLM**, escolha **DeepSeek**.

Documentação: <https://api-docs.deepseek.com/>.

Se o app disser "Licença necessária" ao escolher Gemini ou DeepSeek, a sua licença ainda não está ativa (seção 2).

---

## 6. Voz de emoção (opcional): ElevenLabs

Além das vozes locais (Piper e Kokoro), o app pode usar uma **voz de emoção** na internet. Ela fala os momentos mais fortes da corrida (acidente, líder rodando, ultrapassagem, chegada) com mais expressão.

**Duas vantagens:**

- **Consome menos CPU do seu PC.** As vozes locais são geradas pelo seu processador, o que pesa quando o jogo e a live já usam muito dele. A voz de emoção é gerada nos servidores do serviço e só chega o áudio.
- Soa mais natural e expressiva.

**O preço:** ela precisa de uma **conta no ElevenLabs** e de uma **chave de API pessoal**. Cada fala consome créditos da **sua conta** do ElevenLabs.

### Como configurar o ElevenLabs

1. Crie uma conta em **<https://elevenlabs.io>**.
2. Já logado, abra **<https://elevenlabs.io/app/settings/api-keys>**. Se o endereço mudar, procure **API Keys** no menu da sua conta.
3. Clique para **criar uma chave**, dê um nome (por exemplo "Narrador LMU") e **copie** a chave. Se o ElevenLabs permitir restringir as permissões da chave, deixe só o necessário para gerar voz e listar vozes.
4. No app, aba **Chaves**, bloco **ElevenLabs**: cole e clique em **Salvar chaves**.
5. Aba **Vozes**: escolha o motor **elevenlabs**, clique em **Carregar minhas vozes** e escolha uma voz da sua conta. No plano gratuito, vozes da biblioteca podem ser recusadas pela API: use uma voz **sua** ou da sua lista. Para o narrador e o comentarista soarem diferentes, escolha **vozes diferentes**.
6. Use o botão **Ouvir** para testar. Se falhar, ele mostra o motivo (por exemplo "chave recusada" ou "voz não encontrada").
7. **Reinicie o app** para a mudança de motor valer.

Documentação do ElevenLabs:

- Como a chave de API funciona: <https://elevenlabs.io/docs/api-reference/authentication>
- Primeiros passos: <https://elevenlabs.io/docs/quickstart>
- Planos e preços: <https://elevenlabs.io/pricing>

### Quanto ela cobre da corrida

Na aba **Vozes** a opção **Cobertura** controla o gasto:

| Cobertura | O que fala na voz de emoção |
|---|---|
| **críticos** (padrão) | Só o narrador, nos eventos críticos. O resto fica nas vozes locais. É a opção mais barata. |
| **narrador** | Todas as falas do narrador. |
| **tudo** | Narrador e comentarista, a transmissão inteira. |

Comece em **críticos**. Quanto mais falas na voz de emoção, mais créditos você gasta. O app tem um **limite de chamadas por dia** para proteger o seu bolso: quando acaba, as falas continuam nas vozes locais. Se alguma fala falhar ou demorar, ela sai na voz local e a narração segue.

### Alternativa: Gemini TTS

Se você já tem a chave do Gemini, o motor **gemini** da aba **Vozes** usa a mesma chave, sem criar conta nova. A configuração é a mesma: escolha o motor, a voz, teste com **Ouvir** e reinicie o app.

> A voz de emoção também só funciona com a **licença ativa**.

---

## 7. Atualizar o app

Ao abrir, o app confere se existe uma versão nova e mostra um link na janela principal ("Versão X disponível — baixar"). A atualização é **manual**:

1. Baixe o `.zip` novo em [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases/latest).
2. Feche o app.
3. Extraia a versão nova **numa pasta nova** (não por cima da antiga: o `.zip` traz um `config.toml` padrão que apagaria as suas configurações). Depois **copie** da pasta antiga para a nova os seus arquivos `chaves.toml`, `config.toml` e `licenca.dat`.
4. Abra o app. Se a licença não for reconhecida, ative a chave de novo na aba **Licença**.
5. Quando tudo estiver funcionando, apague a pasta antiga.

Leia as notas de cada versão em [Releases](https://github.com/FelipeSSantos1/LMUNarrador/releases): quando uma versão muda algum valor do `config.toml` que você precise ajustar, isso aparece lá.

---

## 8. Problemas comuns

- **"LMU: aguardando o jogo".** Confira o *Enable Plugins* do jogo (seção 1), feche e abra o LMU por completo, e use o mesmo nível de permissão nos dois.
- **A aba Licença diz "Licença não confirmada".** Falta internet há mais de 7 dias, ou o relógio do Windows está errado. Conecte-se e confira a hora automática. O app tenta de novo sozinho.
- **"Esta licença já está ativa em outro computador".** Use **Desativar este computador** no outro PC, ou fale com o suporte se ele não existe mais.
- **"Licença necessária".** A assinatura não está ativa. Ative a chave (seção 2) ou renove.
- **A IA não fala, só fala pronta.** Falta a chave do Gemini/DeepSeek, a chave foi recusada, ou a conta não tem saldo/cota. Veja a aba **Chaves** e o indicador de LLM na janela principal.
- **A voz de emoção cai na voz normal.** Chave do ElevenLabs ausente ou recusada, voz não encontrada, créditos acabando ou limite diário atingido. Teste com **Ouvir**.
- **Não sai som no OBS.** Escolha o dispositivo do VB-Cable na aba **Geral** e reinicie o app.

Para outros problemas, abra uma *issue* aqui no repositório ou fale com o suporte: **[SEU CONTATO AQUI]**. Se puder, anexe o arquivo da pasta `logs\` (ele não contém as suas chaves).

---

## 9. Privacidade

- As suas chaves de API ficam **só no seu computador**, em `chaves.toml`. O app não as envia para mim nem as grava em log.
- Para validar a licença, o app contata o **Lemon Squeezy** (`api.lemonsqueezy.com`) e envia a **chave de licença** e o **nome do seu computador**. Nada além disso é enviado para a validação, e o app não guarda os seus dados de compra.
- Para escrever as falas, o app envia o **texto dos eventos da corrida** (posições, tempos, incidentes) ao serviço de IA que você escolheu, usando a **sua** chave e sujeito aos termos dele.
- O app não envia a sua telemetria do jogo para nenhum outro lugar.
