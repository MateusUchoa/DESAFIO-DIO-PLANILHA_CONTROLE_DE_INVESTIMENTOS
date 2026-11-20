# Simulador de Investimentos em Fundos Imobiliários (FIIs) e Ações

Este projeto é uma ferramenta desenvolvida em Excel para simular investimentos em Fundos Imobiliários. A planilha permite calcular o crescimento do patrimônio ao longo do tempo e projetar os dividendos mensais com base no perfil do investidor.

## 📊 Perguntas de Negócio que a Ferramenta Responde
A planilha foi construída com "cara de aplicativo" e responde diretamente às seguintes perguntas na tela principal:
- **Quanto investir por mês?** (Definido na área de inputs/configurações)
- **Por quantos anos?** (Definido na área de inputs, projetando cenários de 2 a 30 anos)
- **Qual a taxa de rendimento mensal?** (Calculada e exibida na configuração da carteira)
- **Quanto de patrimônio vai acumular?** (Resultado exibido em destaque no painel principal e na tabela de cenários)
- **Quanto vai receber de dividendos por mês?** (Exibido logo abaixo do patrimônio acumulado)

## 🧮 Lógica de Cálculo: Funções VF e PROCV

- **Função VF (Valor Futuro):** Foi utilizada para calcular o montante acumulado (patrimônio final). Ela considera a taxa de juros mensal (`taxa`), o número de períodos em meses (`nper`), o pagamento constante que é o aporte mensal (`pgto`) e o valor presente (`vp` como 0).
- **Função PROCV com Chave Composta:** Para a divisão inteligente do aporte, criei uma chave composta (concatenando "Perfil" + "Tipo de Fundo") em uma aba de apoio. O `PROCV` busca essa chave exata para retornar o percentual de alocação correto de acordo com a escolha da lista suspensa de validação de dados.

## 🏷️ Intervalos Nomeados Utilizados
Para deixar as fórmulas mais limpas e profissionais, substitui as referências de células por nomes:
- `aporte`: Célula referente ao valor investido mensalmente.
- `taxa_mensal`: Célula com o rendimento mensal esperado da carteira.
- `[Adicione outros que você criou, ex: prazo_anos, salario, etc.]`

## 🍕 Perfis de Investidor e Percentuais
Os percentuais de distribuição por tipo de fundo (Tijolo, Papel, etc.) foram definidos da seguinte forma:
- **[Nome do Perfil 1 - ex: Conservador]:** [Ex: 70% Papel, 30% Tijolo] - *Soma: 100%*
- **[Nome do Perfil 2 - ex: Moderado]:** [Ex: 50% Papel, 50% Tijolo] - *Soma: 100%*
- **[Nome do Perfil 3 - ex: Arrojado]:** [Ex: 30% Papel, 70% Tijolo] - *Soma: 100%*
*(Nota: Estes valores são apenas exemplos para o funcionamento lógico da ferramenta e não configuram recomendação de investimento).*

## 🚀 Evoluções e Melhorias Implementadas
Em relação ao projeto base do Expert, adicionei:
- [Ex: Um gráfico de pizza dinâmico que atualiza conforme o perfil selecionado.]
- [Ex: Ocultação de linhas de grade, barra de fórmulas e guias de planilha para dar imersão de aplicativo.]
- [Ex: Formatação condicional para destacar o melhor cenário de longo prazo.]

## 📸 Capturas de Tela

![Print 1](<img width="715" height="341" alt="Captura de tela 2026-11-20 010504" src="https://github.com/user-attachments/assets/837c3db7-152c-4c61-9908-90181752a8d6" />)
![Print 2](<img width="539" height="187" alt="Captura de tela 2026-11-20 010954" src="https://github.com/user-attachments/assets/db10be77-2994-4f52-9766-ec9713165d8f" />)
![Print 3](<img width="531" height="372" alt="Captura de tela 2026-11-20 010628" src="https://github.com/user-attachments/assets/ef1b83c9-8842-4bf1-94d6-48f00f7bd866" />)
![Print 4](<img width="596" height="413" alt="Captura de tela 2026-11-20 010806" src="https://github.com/user-attachments/assets/40fd2055-cb9c-4e82-b085-588e06395ad5" />)
