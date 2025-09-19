Documentação do Projeto Final
Módulo de HTML5 e CSS3
1. Objetivo Geral
Elaborar um site estático que seja adaptável a qualquer dispositivo e inclusivo para todos os usuários, aplicando recursos do HTML5 com estrutura semântica e estilos avançados em CSS3, explorando Flexbox e Grid, em conformidade com o nível AA da WCAG 2.2.
2. Identificação do Projeto
●	Nome do projeto: Sistema de Gerenciamento de Tarefas
●	Equipe (nomes e RA): Luan Eduardo Bezerra Felix 
●	Repositório (URL): https://github.com/LuanFelix25/ProjetoFinalhtml5css3
●	Resumo:
O sistema de gerenciamento de tarefas é necessário para organizar e acompanhar atividades, aumentar a produtividade, facilitar a priorização e garantir o cumprimento de prazos.
3. Arquitetura de Informação e Páginas
●	Estrutura de diretórios:
/projeto-final/
|-- login.html
|-- cadastro.html
|-- dashboard.html
|-- criar-tarefa.html
|-- tarefa-criada.html
|-- detalhes-tarefa.html
|-- editar-tarefa.html
|-- confirmar-exclusao.html
|-- estiloGlobais.css

●	Mapa do site / páginas previstas:
○	[x] Página de Login (login.html)
○	[x] Página de Cadastro (cadastro.html)
○	[x] Dashboard/Listagem de Tarefas (dashboard.html)
○	[x] Página de Criar Tarefa (criar-tarefa.html)
○	[x] Página de Confirmação de Tarefa Criada (tarefa-criada.html)
○	[x] Página de Detalhes da Tarefa (detalhes-tarefa.html)
○	[x] Página de Edição de Tarefa (editar-tarefa.html)
○	[x] Página de Confirmação de Exclusão (confirmar-exclusao.html)
4. Requisitos
●	Requisitos funcionais (o site deve...):
1.	Permitir que um novo usuário se cadastre com nome completo, e-mail e senha.
2.	Permitir que um usuário existente faça login para acessar sua lista de tarefas.
3.	Permitir a criação, visualização de detalhes, edição e exclusão de tarefas.
●	Requisitos não funcionais (acessibilidade, desempenho, usabilidade, etc.):
1.	O layout da aplicação deve ser totalmente responsivo, adaptando-se a telas de celulares, tablets e desktops.
2.	A aplicação deve ser acessível, garantindo navegação completa via teclado e contraste de cores adequado.
3.	O código deve seguir as boas práticas de semântica do HTML5 e organização do CSS3.
5. Informações Técnicas — HTML5
Semântica essencial: use elementos nativos antes de div/span — header, nav, main, section, article, aside, footer, form.
Acessibilidade: um único <h1> por página; ordem lógica dos headings; texto alternativo em imagens; rótulos associados (<label for>); navegação por teclado; foco visível; contraste mínimo 4.5:1; idioma em <html lang>; link 'pular para o conteúdo'.
●	Boilerplate mínimo com semântica básica (Código Completo de login.html):
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login - Sistema de Gerenciamento de Tarefas</title>
    <link rel="preconnect" href="[https://fonts.googleapis.com](https://fonts.googleapis.com)">
    <link rel="preconnect" href="[https://fonts.gstatic.com](https://fonts.gstatic.com)" crossorigin>
    <link href="[https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap](https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap)" rel="stylesheet">
    <link rel="stylesheet" href="estiloGlobais.css">
</head>
<body>

    <div class="auth-container">
        <header class="auth-header">
            <h1>Sistema de Gerenciamento de Tarefas</h1>
        </header>

        <main>
            <div class="auth-card">
                <h2>Bem-vindo de volta!</h2>
                <form action="dashboard.html" method="get" onsubmit="alert('Login realizado com sucesso!')">
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" placeholder="seu@email.com" value="usuario@exemplo.com" required>
                    </div>
                    <div class="form-group">
                        <label for="senha">Senha</label>
                        <input type="password" id="senha" class="form-control" placeholder="Sua senha" value="123456" required>
                    </div>
                    <button type="submit" class="btn btn-primary">Entrar</button>
                </form>
                <div class="auth-footer-link">
                    <p>Não tem uma conta? <a href="cadastro.html">Cadastre-se</a></p>
                </div>
            </div>
        </main>

        <footer class="site-footer">
            <p>© 2025 Projeto Acadêmico | <a href="#" onclick="alert('Página em desenvolvimento')">Termos de Uso</a></p>
        </footer>
    </div>

</body>
</html>

●	Formulários (Código Completo de cadastro.html):
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cadastro - Sistema de Gerenciamento de Tarefas</title>
    <link rel="preconnect" href="[https://fonts.googleapis.com](https://fonts.googleapis.com)">
    <link rel="preconnect" href="[https://fonts.gstatic.com](https://fonts.gstatic.com)" crossorigin>
    <link href="[https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap](https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap)" rel="stylesheet">
    <link rel="stylesheet" href="estiloGlobais.css">
</head>
<body>

    <div class="auth-container">
        <header class="auth-header">
            <h1>Sistema de Gerenciamento de Tarefas</h1>
        </header>

        <main>
            <div class="auth-card">
                <h2>Criar sua conta</h2>
                <form action="login.html" method="get" onsubmit="alert('Conta criada com sucesso! Faça login para continuar.')">
                    <div class="form-group">
                        <label for="nome">Nome completo</label>
                        <input type="text" id="nome" class="form-control" placeholder="Seu nome completo" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" class="form-control" placeholder="seu@email.com" required>
                    </div>
                    <div class="form-group">
                        <label for="senha">Senha</label>
                        <input type="password" id="senha" class="form-control" placeholder="Mínimo 6 caracteres" minlength="6" required>
                    </div>
                    <div class="form-group">
                        <label for="confirmar-senha">Confirmar senha</label>
                        <input type="password" id="confirmar-senha" class="form-control" placeholder="Confirme sua senha" minlength="6" required>
                    </div>
                    <button type="submit" class="btn btn-primary">Criar conta</button>
                </form>
                <div class="auth-footer-link">
                    <p>Já tem uma conta? <a href="login.html">Fazer login</a></p>
                </div>
            </div>
        </main>

        <footer class="site-footer">
            <p>© 2025 Projeto Acadêmico | <a href="#" onclick="alert('Página em desenvolvimento')">Termos de Uso</a></p>
        </footer>
    </div>

</body>
</html>

6. Informações Técnicas — CSS3
Conceitos: Cascata, Especificidade, Herança; Box Model; Unidades (rem, em, %, vh, vw); Cores (hex, rgb, hsl); Variáveis CSS; Layout (Flexbox/Grid); Media Queries mobile-first; Transições e animações com preferência do usuário (prefers-reduced-motion).
●	Design tokens e responsividade base (Código Completo de estiloGlobais.css):
/* ------------------- */
/* Reset & Variaveis   */
/* ------------------- */
:root {
  --background: #1a202c;
  --surface: #2d3748;
  --primary: #48bb78;
  --primary-hover: #38a169;
  --secondary: #4299e1;
  --secondary-hover: #3182ce;
  --danger: #e53e3e;
  --danger-hover: #c53030;
  --text-primary: #edf2f7;
  --text-secondary: #a0aec0;
  --border-color: #4a5568;
  --font-family: 'Inter', system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: var(--font-family);
  background-color: var(--background);
  color: var(--text-primary);
  line-height: 1.6;
  min-height: 100vh;
}

a {
  color: var(--secondary);
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

img {
  max-width: 100%;
  display: block;
}

h1, h2, h3 {
  color: var(--text-primary);
  line-height: 1.2;
}

/* ------------------- */
/* Layout Autenticação */
/* ------------------- */
.auth-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  padding: 1.5rem;
}

.auth-header {
  text-align: center;
  margin-bottom: 2rem;
}

.auth-header h1 {
  font-size: clamp(1.75rem, 5vw, 2.5rem);
  font-weight: 700;
}

.auth-card {
  background-color: var(--surface);
  padding: 2.5rem;
  border-radius: 0.75rem;
  width: 100%;
  max-width: 450px;
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

.auth-card h2 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
}

.form-group {
  margin-bottom: 1.25rem;
}

.form-group label {
  display: block;
  font-weight: 500;
  margin-bottom: 0.5rem;
  color: var(--text-secondary);
}

.form-control {
  width: 100%;
  padding: 0.75rem 1rem;
  background-color: var(--background);
  border: 1px solid var(--border-color);
  border-radius: 0.375rem;
  color: var(--text-primary);
  font-size: 1rem;
}

.form-control:focus {
  outline: none;
  border-color: var(--secondary);
  box-shadow: 0 0 0 3px rgba(66, 153, 225, 0.5);
}

.btn {
  display: inline-block;
  width: 100%;
  padding: 0.875rem 1rem;
  border: none;
  border-radius: 0.375rem;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  text-align: center;
  transition: background-color 0.2s ease-in-out;
}

.btn-primary {
  background-color: var(--primary);
  color: var(--background);
}

.btn-primary:hover {
  background-color: var(--primary-hover);
}

.btn-secondary {
  background-color: var(--secondary);
  color: #fff;
}
.btn-secondary:hover {
    background-color: var(--secondary-hover);
}


.btn-danger {
  background-color: var(--danger);
  color: #fff;
}
.btn-danger:hover {
    background-color: var(--danger-hover);
}


.auth-footer-link {
  text-align: center;
  margin-top: 1.5rem;
  color: var(--text-secondary);
}

.site-footer {
  text-align: center;
  padding: 1.5rem;
  color: var(--text-secondary);
  font-size: 0.875rem;
}


/* ------------------- */
/* Layout Principal    */
/* ------------------- */
.app-layout {
    display: flex;
    min-height: 100vh;
}

.sidebar {
    background-color: var(--surface);
    width: 250px;
    padding: 2rem 1.5rem;
    display: none; /* Oculto em mobile */
    flex-direction: column;
}

.sidebar-header {
    font-size: 1.75rem;
    font-weight: 700;
    margin-bottom: 2.5rem;
}

.sidebar-nav ul {
    list-style: none;
}

.sidebar-nav li a {
    display: block;
    color: var(--text-secondary);
    padding: 0.75rem 1rem;
    border-radius: 0.375rem;
    font-weight: 500;
    margin-bottom: 0.5rem;
}

.sidebar-nav li a:hover,
.sidebar-nav li a.active {
    background-color: var(--background);
    color: var(--text-primary);
}

.sidebar-footer {
    margin-top: auto;
    font-size: 0.875rem;
    color: var(--text-secondary);
}

.main-content {
    flex: 1;
    padding: 1.5rem;
    overflow-y: auto;
}

.main-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 2rem;
}

.main-header h1 {
    font-size: clamp(1.5rem, 4vw, 2rem);
}

/* Menu Hamburguer */
.mobile-menu-button {
    display: block;
    background: none;
    border: none;
    color: var(--text-primary);
    font-size: 1.5rem;
    cursor: pointer;
    z-index: 1000;
}

/* ------------------- */
/* Componentes         */
/* ------------------- */

/* Dashboard */
.tasks-grid {
    display: grid;
    gap: 1.5rem;
    grid-template-columns: 1fr;
}

.task-card {
    background-color: var(--surface);
    padding: 1.5rem;
    border-radius: 0.75rem;
    display: flex;
    flex-direction: column;
}

.task-card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
}

.task-card-header h3 {
    font-size: 1.25rem;
}

.task-card-body p {
    color: var(--text-secondary);
    margin-bottom: 1.5rem;
    flex-grow: 1;
}

.task-card-footer {
    display: flex;
    gap: 1rem;
}

.task-card-footer .btn {
    flex: 1;
}

/* Detalhes/Edição/Criação de Tarefa */
.task-details-card {
    background-color: var(--surface);
    padding: 2.5rem;
    border-radius: 0.75rem;
    max-width: 800px;
    margin: auto;
}
.task-details-card hr {
    border: none;
    height: 1px;
    background-color: var(--border-color);
    margin: 1.5rem 0;
}
.task-detail-item {
    margin-bottom: 1.5rem;
}
.task-detail-item .label {
    color: var(--text-secondary);
    font-weight: 500;
    margin-bottom: 0.25rem;
}
.task-detail-item .value {
    font-size: 1.125rem;
}

.task-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 1rem;
    margin-top: 2rem;
}

.task-actions .btn {
    width: auto;
    flex-grow: 1;
}

/* ------------------- */
/* Media Queries       */
/* ------------------- */
@media (min-width: 768px) {
    .main-content {
        padding: 2.5rem;
    }

    .tasks-grid {
        grid-template-columns: repeat(2, 1fr);
    }

    .sidebar {
        display: flex;
    }

    .mobile-menu-button {
        display: none;
    }
}

@media (min-width: 1024px) {
    .tasks-grid {
        grid-template-columns: repeat(3, 1fr);
    }
}

7. Plano de Acessibilidade (WCAG 2.2 AA) — Checklist
●	[x] HTML com lang definido (pt-BR).
●	[x] Headings em ordem lógica; apenas um <h1> por página.
●	[x] Landmarks semânticos (header, main, aside, footer).
●	[ ] Link 'Pular para o conteúdo' antes da navegação. (A ser implementado)
●	[x] Texto alternativo descritivo para imagens e ícones (implícito nos botões e links textuais).
●	[x] Links e botões com nomes visíveis e objetivos.
●	[x] Navegação por teclado em 100% dos componentes; foco visível.
●	[x] Contraste mínimo 4.5:1 para texto.
●	[ ] Preferência do usuário respeitada (prefers-reduced-motion). (A ser implementado caso animações complexas sejam adicionadas)
●	[x] Formulários: labels associados aos inputs.
8. Plano de Responsividade — Estratégia
Abordagem: mobile-first. Definir breakpoints principais (ex.: 768px, 1024px). Garantir que o layout não crie scroll horizontal e que componentes reorganizem de forma fluida (Flexbox/Grid). Imagens fluidas e tipografia responsiva.
●	Páginas/alvos de teste:
○	Telefones (~360×640 a 414×896)
○	Tablets (~768×1024)
○	Desktop (≥1366×768)
9. Plano de Testes
Validações e ferramentas sugeridas: W3C HTML/CSS Validators, Lighthouse (Acessibilidade / Performance / SEO), axe DevTools, leitor de tela (NVDA / VoiceOver), navegação por teclado apenas.
Caso de teste	Passos	Resultado esperado	Evidência (URL/captura)	Status
Login com sucesso	1. Abrir login.html. 2. Preencher e-mail/senha. 3. Clicar "Entrar".	Redirecionamento para dashboard.html.	[Anexar captura]	Aprovado
Feedback de criação	1. Acessar criar-tarefa.html. 2. Preencher formulário e salvar.	Retorna ao dashboard.html com a URL #created e exibe a mensagem de sucesso.	[Anexar captura]	Aprovado
Responsividade	1. Abrir dashboard.html. 2. Redimensionar a janela para 375px de largura.	O grid de tarefas se ajusta para uma coluna e a sidebar é ocultada.	[Anexar captura]	Aprovado
Navegação Teclado	1. Abrir login.html. 2. Usar a tecla Tab para navegar.	Todos os campos e botões são focáveis em uma ordem lógica.	[Anexar captura]	Aprovado
10. Plano de Avaliação (0-5)
Critério	Descrição	Pontuação
Estrutura & Semântica HTML5	Correção dos headings, landmarks, links e tabelas.	1
Acessibilidade (WCAG 2.2 AA)	Contraste, foco, navegação por teclado, alt, labels.	1
Responsividade	Layout fluido; quebra adequada nos breakpoints; ausência de overflow.	1
Boas práticas CSS	Organização, variáveis, especificidade controlada, reutilização.	1
Formulários & Feedback	Validação amigável; aria-live; mensagens claras.	0,5
Documentação	Preenchimento deste template com evidências e clareza.	0,5
Total		5
11. Registro de Alterações (Changelog)
Data	Autor	Descrição da alteração	Arquivos impactados
05/09/2025	Luan Felix	feat: Criação da estrutura inicial e telas de autenticação.	login.html, cadastro.html, estiloGlobais.css
05/09/2025	Luan Felix	feat: Desenvolvimento da Dashboard com estados dinâmicos.	dashboard.html, estiloGlobais.css
05/09/2025	Luan Felix	feat: Implementação das telas de CRUD de tarefas.	criar-tarefa.html, editar-tarefa.html, etc.
05/09/2025	Luan Felix	refactor: Ajustes de responsividade e acessibilidade.	estiloGlobais.css, todos os .html
