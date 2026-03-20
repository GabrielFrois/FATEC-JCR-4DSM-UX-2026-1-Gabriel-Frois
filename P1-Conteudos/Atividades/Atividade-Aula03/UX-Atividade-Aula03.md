## Exercício 1 – Criando uma Persona

| Campo | Descrição |
|---|---|
| **Nome (fictício):** | Raimundo Silva |
| **Idade:** | 58 anos |
| **Perfil:** | Produtor rural / Pequeno pecuarista — Sudoeste do Pará (região de Altamira). Propriedade de 40 hectares com gado, mandioca e milho. Ensino fundamental. Aprendeu a usar o celular com o filho mais novo (22 anos). |
| **Objetivos:** | Saber com antecedência se há risco de fogo chegando perto da propriedade para tirar o gado do pasto, acionar vizinhos e ligar para a defesa civil. Quer informação clara e direta, sem precisar interpretar mapas ou termos técnicos. |
| **Frustrações:** | Já tentou o portal do INPE mas desistiu: mapa carregou lento e apareceram "pontinhos vermelhos" sem contexto. Não entende "foco ativo", "risco alto" ou "bioma Amazônia". Ignora alertas genéricos — aprendeu que "coisa de app costuma ser exagero". Sinal 3G instável trava o app antes de carregar. |
| **Tecnologias usadas:** | Smartphone Samsung básico (Android 10) · Conexão 3G instável (piora de manhã e em dias de chuva) · WhatsApp diariamente (grupos de agricultores) · Nunca usou GPS ou app de mapa · Tela no brilho máximo (trabalha ao sol) |
| **Citação:** | *"Eu não preciso de mapa não. Me manda uma mensagem falando: 'Raimundo, tem fogo a 5 km de você, cuidado' — isso eu entendo. Esse negócio de pontinho vermelho no mapa não me diz nada."* |

---

## Exercício 2 – Mapa de Jornada do Usuário

> **Cenário:** Raimundo está no pasto numa tarde seca de agosto quando recebe uma notificação do app INPE.

| Etapa da Experiência | Ação do Usuário | Sentimento | Ponto de Dor | Oportunidade de Melhoria |
|---|---|---|---|---|
| **Antes do alerta** | Está no pasto trabalhando. Celular no bolso. Tela no brilho máximo. Sinal 3G fraco. | Tranquilo. Não pensa no risco de incêndio no momento. | Não tem o hábito de checar o app. Não recebeu nenhuma comunicação prévia sobre como funciona. | Onboarding simples com tutorial de 3 passos ao instalar. Notificação educativa na época seca. |
| **Durante o alerta** | Celular vibra. Abre a notificação. App demora ~8s para carregar. Vê mapa com pontos vermelhos e laranjas. Tenta dar zoom. Lê "foco ativo", "risco alto" e não entende. Liga para o filho. | Ansioso, assustado e frustrado. Pico de ansiedade ao tentar interpretar o mapa sem conseguir. | **CRÍTICO:** Linguagem técnica inacessível. Mapa sem "você está aqui". Carregamento lento. Depende do filho para interpretar — perde autonomia em momento urgente. | Notificação em linguagem natural: *"Fogo a 12 km de você — fique atento"* · GPS automático "Você está aqui" · Distância em km do foco · App leve para 3G |
| **Depois do alerta** | Com ajuda do filho, entende que o foco está a 12 km. Tira o gado do pasto. Manda mensagem no grupo do WhatsApp dos vizinhos avisando. | Aliviado, mas cansado pela dificuldade. Resolve agir por precaução. | A resolução dependeu de uma terceira pessoa. Sem o filho, teria ignorado ou interpretado errado. | Botão "Compartilhar no WhatsApp" com mensagem pronta · Card de ação: *"O que fazer agora?"* · Confirmação clara: *"Você está seguro por enquanto"* |

---

## Exercício 3 – Identificando Pontos Críticos

| Momento Crítico | Por que é crítico? | Solução sugerida pelo App |
|---|---|---|
| **Notificação com linguagem técnica** | Raimundo não sabe se o alerta é urgente ou apenas informativo. O termo "foco ativo" não comunica risco de forma imediata para quem não tem formação técnica. | Reescrever a notificação em linguagem natural: *"Fogo detectado a 12 km de você. Fique atento."* + ícone visual de nível de risco (verde / amarelo / vermelho). |
| **Mapa sem referência espacial** *Pico crítico* | Sem "você está aqui", Raimundo não consegue identificar se o foco está perto ou longe da sua fazenda. Um mapa com dezenas de pontos sem contexto gera pânico desnecessário ou descaso. | Mostrar automaticamente a localização do usuário via GPS ao abrir o app · Exibir apenas os focos mais próximos (raio configurável) · Mostrar distância em km no card do alerta. |
| **Dependência de terceiros para interpretar** | Raimundo precisou ligar para o filho para entender o alerta. Em uma situação real de emergência, esse tempo perdido pode ser crítico. O app falhou em ser autossuficiente para esse perfil de usuário. | Card de resumo simples após o alerta: *"O que aconteceu / Onde está / O que fazer agora"* · Botão "Compartilhar no WhatsApp" com mensagem já formatada para avisar vizinhos. |