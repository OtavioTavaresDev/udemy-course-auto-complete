// Função para expandir todas as seções colapsadas
function expandirTodasSecoes() {
    document.querySelectorAll('[data-purpose="section-panel"] button[aria-expanded="false"]').forEach(btn => btn.click());
    console.log('🔄 Expandindo seções... Aguarde.');
}

// Função principal para marcar itens pendentes (MAIS LENTA PARA EVITAR LOGOUT)
function marcarItensPendentes() {
    const botoes = document.querySelectorAll('[data-purpose="progress-toggle-button"]');
    const pendentes = Array.from(botoes).filter(btn => btn.checked === false);
    
    console.log(`✅ Encontrados ${pendentes.length} itens para marcar.`);
    console.log(`⏳ Marcando 1 item por segundo para evitar bloqueio...`);
    
    if (pendentes.length === 0) {
        console.log('🏁 Nenhum item pendente. Atualize a página (F5) para ver as barras verdes.');
        return;
    }

    let index = 0;
    function clicarProximo() {
        if (index < pendentes.length) {
            pendentes[index].click();
            
            // Mostra progresso a cada 10 itens
            if ((index + 1) % 10 === 0) {
                console.log(`📌 Progresso: ${index + 1}/${pendentes.length} itens marcados.`);
            }
            
            index++;
            // ⚠️ AUMENTADO PARA 1000ms (1 segundo) para evitar logout
            setTimeout(clicarProximo, 1000); 
        } else {
            console.log('🎉 Todos os itens foram marcados com sucesso!');
            console.log('💡 Agora você pode recarregar a página (F5) SEM medo de ser deslogado.');
        }
    }
    clicarProximo();
}

// Executa a expansão e agenda a marcação
expandirTodasSecoes();

setTimeout(() => {
    marcarItensPendentes();
}, 3000);
