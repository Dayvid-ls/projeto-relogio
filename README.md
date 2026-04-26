# Projeto Relógio 🕒

Relógio digital simples e elegante que exibe a hora atual (horário de Brasília) com atualização dinâmica a cada segundo. Desenvolvido com HTML, CSS e JavaScript puro.

## Tecnologias usadas
- HTML5
- CSS3 (gradientes, flexbox, sombras, fontes customizadas)
- JavaScript (manipulação do DOM, setInterval, formatação de horário)

## Funcionalidades
- Exibição do horário no formato HH:MM:SS
- Atualização automática a cada segundo
- Formatação de números com dois dígitos (ex: 09:05:03)
- Fundo com gradiente linear
- Relógio estilizado com gradiente, sombra e fonte personalizada
- Subtítulo "Horário de Brasília" abaixo do relógio

## Como executar
1. Baixe todos os arquivos na mesma pasta:
2. Abra o arquivo `index.html` em qualquer navegador moderno.

## Funcionalidades em detalhe

| Função | Descrição |
|--------|-----------|
| `atualizarTempo()` | Obtém a hora atual do sistema, formata com `corrigirHorario()` e atualiza o elemento `.display` |
| `corrigirHorario(numero)` | Adiciona zero à esquerda se o número for menor que 10 |
| `setInterval(atualizarTempo, 1000)` | Executa a atualização a cada 1000 milissegundos (1 segundo) |
| `atualizarTempo()` chamada inicial | Garante que o horário seja exibido imediatamente ao carregar a página |

## Estilos e visuais
- **Fundo da página**: gradiente linear de azul para roxo (`#3fadff` → `#e4d3ea` → `#af36ff`)
- **Container `.relogio`**: ocupa 100% da altura da tela (`height: 100vh`) e centraliza o conteúdo com flexbox
- **Display do relógio**: gradiente de rosa para roxo, largura 300px, altura 200px, texto centralizado verticalmente (`line-height: 200px`), fonte `Qahiri` de 7rem, borda arredondada e sombra
- **Footer**: fonte `Barlow Condensed`, tamanho 2rem, cor cinza

## Observações
- O relógio utiliza a **hora local do sistema** do usuário. Para exibir especificamente o "Horário de Brasília", é necessário que o sistema operacional esteja configurado no fuso horário de Brasília (UTC-3). Em uma melhoria futura, pode-se forçar o fuso manualmente.
- O código JavaScript contém um pequeno erro: `console.log(horario)` está fora da função `atualizarTempo()`, onde a variável `horario` não foi definida. Isso não impede o funcionamento do relógio, mas gera um erro no console do navegador. A correção é mover o `console.log` para dentro da função.

## Possíveis melhorias futuras
- Adicionar suporte a fuso horário fixo (ex: sempre exibir horário de Brasília independente da configuração do sistema)
- Incluir data (dia/mês/ano)
- Adicionar tema claro/escuro com botão de alternância
- Tornar o relógio responsivo para telas menores (ajustar tamanho da fonte)
- Adicionar animação suave ao mudar os números
- Exibir também os segundos com animação de "piscar" dos dois pontos

---
