# 💱 Agente de IA para Cotação de Moedas (n8n)


Automação low-code construída no n8n: Agente de IA especialista em finanças e câmbio, com memória de conversa e capacidade de consultar cotações de moedas em tempo real.



O agente conversa em linguagem natural sobre câmbio e finanças. Sempre que o usuário pergunta pela cotação de uma moeda, o agente usa HTTP Request para buscar o valor atualizado na AwesomeAPI antes de responder, para consultar dados reais. Além disso, o agente mantém o histórico da conversa através de memória persistente no Redis, permitindo diálogos com contexto.