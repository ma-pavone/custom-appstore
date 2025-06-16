<<<<<<< HEAD
🚀 Runtipi Control Panel
Docker
Python
Flask
Runtipi

Painel de controle web elegante para gerenciar suas aplicações Runtipi remotamente

Runtipi Control Panel Preview

✨ Características
🎯 Interface Web Moderna - Dashboard responsivo e intuitivo
⚡ Controle Instantâneo - Start/Stop de aplicações com um clique
📊 Monitoramento em Tempo Real - Status das aplicações atualizado automaticamente
🔒 Autenticação Segura - Integração nativa com credenciais do Runtipi
📱 Mobile Friendly - Interface totalmente responsiva
🌐 API REST - Endpoints para integração com outros sistemas
🔄 Auto-Refresh - Atualização automática a cada 30 segundos
💾 Persistência de Dados - Configurações salvas automaticamente
🎨 Interface
Dashboard Principal
Status Global - Indicador de conexão e contadores
Grid de Aplicações - Cards elegantes com informações detalhadas
Controle Direto - Botões de start/stop por aplicação
Notificações - Feedback visual das operações
Recursos Visuais
Gradientes Modernos - Design visual atrativo
Animações Suaves - Transições e hover effects
Status Indicators - Cores e ícones intuitivos
Responsive Design - Funciona em desktop, tablet e mobile
🚀 Instalação
1. Preparar o App
bash



# Criar diretório do app
mkdir -p ~/runtipi/apps/migrated/runtipi-control/{app/templates}
cd ~/runtipi/apps/migrated/runtipi-control
2. Criar Arquivos de Configuração
Copie os arquivos fornecidos:

config.json - Configuração do app Runtipi
docker-compose.yml - Definição dos containers
app/app.py - Aplicação Python/Flask
app/templates/index.html - Interface web
3. Instalar via Runtipi
Acesse a interface web do Runtipi
Vá em Apps → Local Apps
Encontre "Runtipi Control"
Clique em Install
4. Configurar Credenciais
Durante a instalação, configure:

Campo	Descrição	Exemplo
Runtipi Host	URL do seu servidor Runtipi	localhost:3000
Username	Seu usuário do Runtipi	admin
Password	Sua senha do Runtipi	sua_senha_segura
🎯 Como Usar
Acessar o Painel
http://seu-servidor:8300
Funcionalidades Principais
🎮 Controle de Aplicações
Toggle Inteligente - Clique no botão para alternar start/stop
Status Visual - Cards coloridos indicam se a app está rodando ou parada
Feedback Instantâneo - Notificações confirmam as operações
📊 Monitoramento
Contador Global - Quantas apps estão rodando vs total
Status de Conexão - Indicador visual da comunicação com Runtipi
Auto-Refresh - Dados atualizados automaticamente
🔄 Atualização Manual
Botão "Atualizar" para refresh imediato
Útil após mudanças externas no Runtipi
🛠️ API Endpoints
GET /api/apps
json



{
  "installed": [
    {
      "info": {
        "id": "app-name",
        "name": "App Display Name",
        "short_desc": "Description"
      },
      "app": {
        "status": "running",
        "port": 8080
      }
    }
  ]
}
POST /api/toggle
json



{
  "appId": "nome-da-aplicacao"
}
Resposta:

json



{
  "success": true,
  "message": "✅ Start executado com sucesso",
  "action": "start",
  "previous_status": "stopped",
  "app_name": "Nome da App"
}
GET /api/status
json



{
  "status": "ok",
  "apps_running": 5,
  "apps_total": 12,
  "runtipi_host": "localhost:3000",
  "timestamp": "2024-01-15T10:30:00"
}
🔧 Configuração Avançada
Variáveis de Ambiente
bash



RUNTIPI_HOST=localhost:3000          # Host do Runtipi
RUNTIPI_USERNAME=admin               # Usuário de acesso
RUNTIPI_PASSWORD=senha               # Senha de acesso
FLASK_HOST=0.0.0.0                  # Host do Flask
FLASK_PORT=8080                     # Porta interna
FLASK_DEBUG=false                   # Debug mode
Personalização
python



# Modificar app/app.py para:
# - Alterar intervalo de refresh
# - Adicionar novos endpoints
# - Customizar autenticação
# - Implementar logs avançados
🐛 Troubleshooting
❌ App não aparece na lista
bash



# Verificar estrutura
ls -la ~/runtipi/apps/migrated/runtipi-control/

# Reiniciar Runtipi
cd ~/runtipi
docker compose restart
❌ Erro de autenticação
Verificar se as credenciais estão corretas
Confirmar se o Runtipi está acessível
Checar logs: docker logs runtipi-control
❌ Aplicações não carregam
bash



# Verificar conectividade
curl http://localhost:3000/api/apps/installed

# Verificar logs
docker logs runtipi-control
📁 Estrutura do Projeto
runtipi-control/ ├── config.json # Configuração do app Runtipi ├── docker-compose.yml # Definição dos containers ├── README.md # Este arquivo └── app/ ├── app.py # Aplicação Python/Flask └── templates/ └── index.html # Interface web
🤝 Contribuindo
Fork o projeto
Crie uma branch para sua feature
Commit suas mudanças
Push para a branch
Abra um Pull Request
💡 Ideias para Contribuição
 Suporte a temas dark/light
 Filtros e busca de aplicações
 Logs em tempo real das aplicações
 Estatísticas de uso e performance
 Notificações push/email
 Backup/restore de configurações
📄 Licença
Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

🙏 Agradecimentos
Runtipi Team - Pela excelente plataforma de self-hosting
Flask Community - Pelo framework web robusto
Docker - Por simplificar o deployment

Feito com ❤️ para a comunidade Runtipi
🐛 Report Bug · ✨ Request Feature · 💬 Discord
=======
# local-apps-runtipi
>>>>>>> 1c502400e1e7182e6e1afc323ce558a1fa41323f
