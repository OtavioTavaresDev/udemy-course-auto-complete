# Udemy Course Auto-Complete 🚀

Script para marcar automaticamente todas as aulas de um curso da Udemy como concluídas.

> ⚠️ **Use com responsabilidade**: Este script é útil para cursos que você já assistiu ou quando a Udemy não registra corretamente seu progresso.

## 📖 Por que criei este script?

Em 2024, completei alguns cursos na Udemy e, após finalizar todas as aulas, segui com outros projetos. Meses depois, ao acessar novamente a plataforma, percebi que **nenhum dos cursos estava marcado como concluído** e várias aulas individuais também não haviam sido registradas como assistidas.

Como já havia dedicado horas ao conteúdo e não queria refazer todo o processo manualmente (clicar em centenas de checkboxes, uma por uma), desenvolvi este script para automatizar a marcação do que eu já havia estudado legitimamente.

Se você está na mesma situação — seja por um bug da Udemy, por ter assistido aulas offline, ou por ter migrado de conta — este script vai te poupar **horas de cliques repetitivos**.

## 🎯 Funcionalidades

- ✅ Expande automaticamente todas as seções do curso
- ✅ Marca todas as aulas pendentes como concluídas
- ✅ Duas versões disponíveis:
  - **Rápida**: Marca todos os itens em segundos (pode causar logout)
  - **Segura**: Intervalo de 1 segundo entre cliques (recomendada)

## 📥 Como usar

### Método 1: Console do Navegador (Recomendado)

1. Acesse a página do seu curso na Udemy
2. Role até o final da página (para carregar todo o conteúdo)
3. Abra o Console do desenvolvedor:
   - **Windows/Linux**: `Ctrl + Shift + J` ou `F12`
   - **Mac**: `Cmd + Option + J`
4. Cole o código da versão desejada e pressione `Enter`

### Método 2: Bookmarklet (Em breve)

Crie um favorito com o código para executar com um clique.

## 📊 Comparação das Versões

| Versão | Intervalo | Velocidade | Risco de Logout | Quando usar |
|--------|-----------|------------|-----------------|-------------|
| **fast-version.js** | 150ms | ~15 itens/seg | Alto | Cursos pequenos (< 30 aulas) |
| **safe-version.js** | 1000ms | 1 item/seg | Baixo | Cursos grandes ou quando já foi deslogado |

## 🔧 Solução de Problemas

### ❌ "Encontrados 0 itens para marcar"

**Causa**: Seções não expandidas ou conteúdo não carregado.

**Solução**: 
1. Role manualmente até o final da página
2. Clique para expandir todas as seções manualmente
3. Execute o script novamente

### ❌ Fui deslogado durante a execução

**Causa**: Muitas requisições em pouco tempo.

**Solução**: Use a `safe-version.js` com intervalo de 1000ms.

### ❌ Erros vermelhos no console (`ERR_BLOCKED_BY_CLIENT`)

**Causa**: Seu AdBlock está bloqueando a telemetria da Udemy.

**Impacto**: **Nenhum** no funcionamento do script. Ignore esses erros.

## 🤝 Contribuindo

Contribuições são bem-vindas! Se você encontrou um bug ou tem uma melhoria:

1. Abra uma Issue descrevendo o problema
2. Envie um Pull Request com a solução

## ⚖️ Licença

MIT License - Veja o arquivo [LICENSE](LICENSE) para detalhes.

## ⭐ Agradecimentos

Este script foi desenvolvido para resolver um problema real enfrentado por estudantes da Udemy. Se foi útil para você, considere dar uma estrela no repositório!

---
**Nota**: Este projeto não é afiliado, associado, autorizado, endossado ou de qualquer forma oficialmente conectado à Udemy.
