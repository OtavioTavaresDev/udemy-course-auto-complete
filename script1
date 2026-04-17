// Função para expandir todas as seções colapsadas
function expandirTodasSecoes() {
    document.querySelectorAll('[data-purpose="section-panel"] button[aria-expanded="false"]').forEach(btn => btn.click());
    console.log('🔄 Expandindo seções... Aguarde.');
}

// Função principal para marcar itens pendentes
function marcarItensPendentes() {
    // Seleciona todos os botões de progresso que NÃO estão marcados
    const botoes = document.querySelectorAll('[data-purpose="progress-toggle-button"]');
    const pendentes = Array.from(botoes).filter(btn => btn.checked === false); // ou !btn.checked
    
    console.log(`✅ Encontrados ${pendentes.length} itens para marcar.`);
    
    if (pendentes.length === 0) {
        console.log('🏁 Nenhum item pendente. Atualize a página (F5) para ver as barras verdes.');
        return;
    }

    let index = 0;
    function clicarProximo() {
        if (index < pendentes.length) {
            pendentes[index].click();
            index++;
            setTimeout(clicarProximo, 150); // Intervalo para não sobrecarregar
        } else {
            console.log('🎉 Todos os itens foram marcados! Recarregue a página (F5) para atualizar o progresso.');
        }
    }
    clicarProximo();
}

// Executa a expansão e agenda a marcação para depois do carregamento
expandirTodasSecoes();

// Aguarda 3 segundos para a Udemy carregar os itens das seções expandidas
setTimeout(() => {
    // Algumas seções podem ter muitos itens, damos mais uma verificada rápida
    marcarItensPendentes();
}, 3000);
