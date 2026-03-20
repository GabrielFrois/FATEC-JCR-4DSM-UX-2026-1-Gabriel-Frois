## Exercício 1 – Fluxo de Usuário Simples

Fluxo linear da persona Raimundo ao receber e agir sobre um alerta de foco de calor. Sem ramificações — representa o caminho ideal (*happy path*).

### Diagrama do Fluxo

```
■ INÍCIO              ■ Recebe Alerta       ■ Abre o App          ■ Vê Localização      ■ Entende o Risco     ■ Age
App instalado.   →    Celular vibra com  →  Toca na notificação. → 'Você está aqui'  →  Card simples:      →  Tira gado do pasto.
Notificação           push notification.    App carrega.           aparecer no mapa.     'Fogo a 12 km —       Avisa vizinhos.
ativada.                                                                                 Médio'
```

> Fluxo linear: cada etapa leva obrigatoriamente à próxima, sem desvios.

### Tabela de Etapas

| Etapa | O que acontece | Tela / Componente do App |
|---|---|---|
| ■ Início | App instalado, notificação push ativada. | Tela de boas-vindas / permissões |
| ■ Recebe Alerta | Celular vibra. Push aparece na tela de bloqueio. | Notificação do sistema (push) |
| ■ Abre o App | Raimundo toca na notificação. App abre em ~3s. | Tela de carregamento + splash |
| ■ Vê Localização | Mapa centraliza no usuário. Foco mais próximo destacado. | Tela principal — Mapa com GPS |
| ■ Entende o Risco | Card simples: "Fogo a 12 km de você — Risco Médio". | Card de alerta em linguagem natural |
| ■ Age | Tira gado do pasto. Compartilha alerta no WhatsApp. | Botão "Compartilhar no WhatsApp" |

---

## Exercício 2 – Fluxo Refinado com Decisões Alternativas

Adicionadas 2 decisões alternativas: **(1)** app instalado? e **(2)** usuário entende o alerta? Cada "NÃO" redireciona para um caminho de suporte.

### Diagrama do Fluxo

```
■ INÍCIO
App instalado.
Notificação ativada.
        ↓
■ Recebe Alerta
Push notification no celular.
        ↓
◆ App Instalado?
  ├── SIM ↓
  │     ■ Abre o App
  │     Toca na notificação. App carrega.
  │           ↓
  │     ◆ Entende o Alerta?
  │       ├── NÃO ←
  │       │     ■ Ver Tutorial
  │       │     Glossário rápido: 'foco ativo = fogo agora'
  │       └── SIM ↓
  │             ■ Vê Localização
  │             'Você está aqui' · Fogo a 12 km — Médio
  │                   ↓
  │             ■ Age
  │             Tira gado. Avisa vizinhos no WhatsApp.
  └── NÃO →
        ■■ Instalar App
        Redireciona para a loja de apps.
```

### Tabela de Decisões

| Decisão | Caminho SIM | Caminho NÃO (alternativo) | Por que isso existe? |
|---|---|---|---|
| App instalado? | Abre o app normalmente | Redireciona para instalar na loja | Raimundo só instalou o app porque o filho mandou — pode tentar abrir sem ter instalado. |
| Entende o alerta? | Avança para ver localização no mapa | Abre tutorial com glossário rápido ("foco ativo = fogo agora") | Raimundo não sabe termos técnicos. O app precisa ter uma saída de aprendizado rápido. |

---

## Exercício 3 – Relação entre o Fluxo e o Mapa de Jornada

Como o Fluxo de Usuário (Aula 04) se conecta ao Mapa de Jornada construído na Aula 03.

| Etapa do Fluxo | Etapa da Jornada (Aula 03) | Emoção identificada na Jornada | Como o Fluxo resolve o ponto de dor |
|---|---|---|---|
| ■ App instalado / Notificação ativada | ANTES do alerta | Tranquilo (sem consciência do risco) | Onboarding simples com tutorial de 3 passos ao instalar. Notificação educativa na época seca. |
| ■ Recebe Alerta / Push na tela | DURANTE o alerta (início) | Ansioso — "O que é isso?" | Notificação em linguagem natural: "Fogo a 12 km — fique atento". Ícone de cor para nível de risco. |
| ■ Abre o App / Decisão: instalado? | DURANTE o alerta (abertura) | Impaciente — "Por que demora?" | Barra de progresso visível. App versão leve para 3G. Fluxo alternativo se não instalado. |
| ■ Vê Localização / GPS automático | DURANTE o alerta (mapa) | Assustado — "Onde é minha fazenda?" | "Você está aqui" ativado automaticamente. Mostra distância em km, não apenas ponto no mapa. |
| ■ Entende o Risco / Decisão: entende? | DURANTE o alerta **(PICO CRÍTICO ■■)** | Frustrado — "O que é foco ativo?" | Card simples: "Fogo a 12 km · Risco Médio · Detectado hoje às 14h". Fluxo alternativo com tutorial/glossário. |
| ■ Age / Compartilha WhatsApp | DEPOIS do alerta | Aliviado (mas dependeu do filho) | Botão "Compartilhar no WhatsApp" com mensagem já formatada. Card "O que fazer agora?" com 3 passos simples. |

### Síntese

> **O Fluxo de Usuário é o *como*** — define as telas e decisões técnicas do app.
> **O Mapa de Jornada é o *porquê*** — revela as emoções e dores que motivam cada decisão de design.
> Juntos, eles garantem que o app resolva os problemas reais de Raimundo, não apenas os técnicos.
