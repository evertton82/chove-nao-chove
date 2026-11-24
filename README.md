# Chove Não Chove

Aplicativo de previsão do tempo feito em React Native com Expo e Expo Router.
Trabalho final da matéria.

## Objetivo

Mostrar o tempo de agora e a previsão dos próximos 7 dias para uma cidade escolhida pelo usuário,
respondendo de forma direta a pergunta: vai chover hoje?

## Tecnologias (todas gratuitas)

- **React Native + Expo**: desenvolvimento do app
- **Expo Go**: execução no celular
- **Expo Router**: navegação entre telas, com layout raiz
- **Open-Meteo**: API de previsão do tempo e de busca de cidade, sem cadastro e sem chave
- **@expo/vector-icons**: ícones (já vem com o Expo)

## Telas

```
app/
  _layout.js     layout raiz: navegação em pilha (Stack), cor e título do cabeçalho
  index.js       Início: tempo agora e "Vai chover hoje?"
  buscar.js      Buscar cidade: digita o nome e escolhe na lista
  previsao.js    Próximos 7 dias da cidade escolhida
  sobre.js       Sobre o app: autor, matéria e crédito da Open-Meteo
```

### Layout raiz
Define a pilha de telas, o título de cada uma e a cor do cabeçalho.

### Início
- Cidade, temperatura, sensação térmica, descrição em português, ícone, umidade e vento
- Destaque "Vai chover hoje?" com a chance de chuva em %
- Botões: Trocar cidade, Próximos dias e Sobre

### Buscar
- Campo para digitar o nome da cidade
- Lista de resultados vinda da API de geocodificação da Open-Meteo
- Ao tocar em um resultado, volta ao Início com a cidade escolhida

### Previsão
- Recebe a cidade por parâmetro de rota
- Lista os 7 dias: dia da semana, ícone, mínima, máxima e chance de chuva

### Sobre
- Informações do trabalho e link para a Open-Meteo

## Regras do app

- O código do tempo da Open-Meteo (número) é traduzido para texto em português e ícone
- Estados tratados: carregando, cidade não encontrada e sem internet
- A cor de fundo muda conforme o tempo (sol, nublado, chuva)
- O app abre com uma cidade inicial já carregada

## Conceitos de Expo Router usados

- Layout raiz (`app/_layout.js`)
- Navegação em pilha com `Stack`
- Navegação com `Link` e `router.push`
- Passagem de parâmetros entre telas com `useLocalSearchParams`
- Título do cabeçalho definido por tela

## Fora do escopo (melhorias futuras)

- Localização por GPS
- Cidades favoritas salvas
- Login de usuário
- Notificações

## Etapas

| # | Etapa | Situação |
|---|---|---|
| 1 | README com o escopo | Feito |
| 2 | Criar o projeto Expo com Expo Router | A fazer |
| 3 | Layout raiz e as 4 telas navegando entre si | A fazer |
| 4 | Tabela de códigos do tempo | A fazer |
| 5 | Início com dados reais da Open-Meteo | A fazer |
| 6 | Tela Buscar e retorno da cidade escolhida | A fazer |
| 7 | Tela Previsão de 7 dias | A fazer |
| 8 | Carregando, erros e cor de fundo | A fazer |
| 9 | Tela Sobre e README final com prints | A fazer |

## Fonte dos dados

Dados meteorológicos fornecidos por [Open-Meteo](https://open-meteo.com) (licença CC BY 4.0).
