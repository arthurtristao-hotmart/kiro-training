---
theme: default
title: Treinamento KIRO
info: |
  ## Treinamento KIRO
  Instalação, setup, ferramentas e Spec-Driven Development.
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  sans: Inter
  mono: Fira Code
---

<div class="flex flex-col items-center justify-center h-full">
  <div class="text-[var(--kiro-purple-light)] mb-4">
    <KiroMark size="88" />
  </div>
  <div class="text-[var(--kiro-text)]">
    <KiroWordmark :width="320" />
  </div>
  <p class="mt-6 text-xl kiro-dim">Agentic IDE — da spec à produção</p>
  <p class="mt-10 kiro-chip">Treinamento interno · Spec-Driven Development</p>
</div>

<div class="abs-br m-6 text-sm kiro-dim">
  Pressione <kbd>Espaço</kbd> para avançar <carbon:arrow-right class="inline" />
</div>

<!--
Capa. Apresente o Kiro em uma frase: um IDE agentic que transforma prompts em
specs, designs e tarefas, e as executa com agentes. Hoje: instalar, autenticar,
conhecer as ferramentas e colocar a mão na massa com SDD.
-->

---
layout: center
---

<div class="h-full flex flex-col justify-center">
<div class="grid grid-cols-2 gap-10 max-w-4xl mx-auto w-full">
<!-- ===== DEV 1 ===== -->
<div class="kiro-card flex flex-col items-center text-center">
<img src="/arthur.jpg" class="kiro-photo object-cover" alt="Foto do Arthur" />
<div class="text-2xl font-bold text-[var(--kiro-text)] mt-5">Arthur Tristão</div>
<div class="kiro-dim text-sm mt-3 uppercase tracking-wide">Cargo</div>
<div class="text-base">Software Engineer Intern</div>
<div class="kiro-dim text-sm mt-2 uppercase tracking-wide">Time</div>
<div class="text-base">Club Setup</div>
</div>
<!-- ===== DEV 2 ===== -->
<div class="kiro-card flex flex-col items-center text-center">
<img src="/saymon.png" class="kiro-photo object-cover" alt="Foto do Saymon" />
<div class="text-2xl font-bold text-[var(--kiro-text)] mt-5">Saymon Silva</div>
<div class="kiro-dim text-sm mt-3 uppercase tracking-wide">Cargo</div>
<div class="text-base">Staff Engineer I</div>
<div class="kiro-dim text-sm mt-2 uppercase tracking-wide">Time</div>
<div class="text-base">DACP</div>
</div>
</div>
</div>



---
layout: center
class: text-center
---

# O que vamos ver hoje

<div class="grid grid-cols-2 gap-5 mt-8 text-left max-w-3xl mx-auto">
  <div class="kiro-card flex items-start gap-3">
    <span class="kiro-step-num">1</span>
    <div>
      <div class="font-bold">Instalação do Kiro</div>
      <div class="kiro-dim text-sm">Solicitar acesso, verificar e instalar</div>
    </div>
  </div>
  <div class="kiro-card flex items-start gap-3">
    <span class="kiro-step-num">2</span>
    <div>
      <div class="font-bold">Autenticação & Setup inicial</div>
      <div class="kiro-dim text-sm">Login via AWS IAM Identity Center</div>
    </div>
  </div>
  <div class="kiro-card flex items-start gap-3">
    <span class="kiro-step-num">3</span>
    <div>
      <div class="font-bold">Ferramentas</div>
      <div class="kiro-dim text-sm">Steering, Skills, MCPs e mais — ao vivo</div>
    </div>
  </div>
  <div class="kiro-card flex items-start gap-3">
    <span class="kiro-step-num">4</span>
    <div>
      <div class="font-bold">Hands On — SDD</div>
      <div class="kiro-dim text-sm">Spec-Driven Development na prática</div>
    </div>
  </div>
</div>

<!--
Agenda. Partes 1 e 2 são guiadas; a 3 é mais demonstração ao vivo; a 4 é
mão na massa com todos acompanhando.
-->

---
layout: center
class: text-center
---

<div class="flex flex-col items-center">
  <span class="kiro-chip mb-6">PARTE 1</span>
  <div class="text-[var(--kiro-purple-light)] mb-4"><KiroMark size="56" /></div>
</div>

# Instalação do Kiro

<div class="flex flex-col items-center"><p class="kiro-dim mt-2">Solicitação de acesso, verificação e instalação</p>
<a
  href="https://hotmart.atlassian.net/wiki/spaces/platform/pages/2509799555/Configura+o+do+KIRO"
  target="_blank"
  class="kiro-chip inline-flex items-center gap-2 hover:opacity-80 transition no-underline"
>
  <carbon:launch /> Configurando o KIRO
</a>
<SkipButton :to="15" label="⏭ Pular Tutorial" /></div>


<!--
Esta parte segue o fluxo oficial da Hotmart: o acesso ao Kiro é concedido via
AWS (perfil Amazon-Kiro-Pro-Plus na conta buildstaging), então antes de instalar
é preciso solicitar e aguardar a liberação do acesso.
-->

---

# Passo 1 — Solicitar acesso ao KIRO

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

O acesso ao Kiro é solicitado pelo **IT Service Desk**.

<div class="kiro-card mt-4">
  <div class="kiro-accent font-bold mb-1">🔗 Link para solicitação</div>
  <div class="text-sm">
    <a href="https://hotmart.atlassian.net/servicedesk/customer/portal/4/group/345/create/3641">IT Service Desk — Concessão de Acesso</a>
  </div>
</div>

<div class="kiro-card mt-4">
  <div class="font-bold mb-1">Como preencher o chamado</div>
  <ul class="text-sm kiro-dim leading-relaxed">
    <li><b>Sistema:</b> AWS - Kiro</li>
    <li><b>Perfil / Banco:</b> <code>AWS_hotmart_Kiro_Pro</code></li>
    <li><b>Resumo:</b> Solicitar acesso para o AWS - Kiro</li>
  </ul>
</div>

</div>
<div>

<img src="/pdf/01-servicedesk-form.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Formulário do IT Service Desk para concessão de acesso" />

</div>
</div>

<!--
Ao vivo (opcional): abra o formulário e mostre o preenchimento. Reforce o perfil
exato AWS_hotmart_Kiro_Pro — é o que libera o Kiro.
-->

---

# Passo 2 — Verificar a concessão de acesso

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

Após a aprovação do ticket, em algumas horas o acesso é concedido na sua **conta AWS**.

Acesse o **AWS Access Portal** por uma das opções:

<div class="kiro-card mt-3">
  <div><span class="kiro-accent font-bold">OKTA</span><br><a href="https://hotmart.okta.com/app/UserHome" class="text-sm">hotmart.okta.com/app/UserHome</a></div>
  <div class="mt-3"><span class="kiro-accent font-bold">AWS Direto</span><br><a href="https://d-90671335e2.awsapps.com/start/#/" class="text-sm">d-90671335e2.awsapps.com/start</a></div>
</div>

<div class="kiro-card mt-4">
  Verifique se o perfil <b class="kiro-accent">Amazon-Kiro-Pro-Plus</b> está disponível na conta <b class="kiro-accent">buildstaging</b>.
</div>

</div>
<div>

<img src="/pdf/02-okta-myapps.png" class="rounded-lg border border-[var(--kiro-border)] w-full mb-3" alt="Okta My Apps com AWS Single Sign-On destacado" />
<img src="/pdf/03-aws-access-portal.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="AWS access portal mostrando Amazon-Kiro-Pro-Plus na conta buildstaging" />

</div>
</div>

<!--
Ao vivo: mostre o portal. Se o perfil não aparecer, ainda não liberou — pode
levar horas (ver slide de erro no fim).
-->

---

# Passo 3 — Instalar o KIRO IDE e CLI

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

Instale o **KIRO IDE** para aproveitar melhor os recursos próprios da IDE.

<div class="kiro-card mt-4">
  <div class="kiro-accent font-bold mb-1">🔗 Download</div>
  <a href="https://kiro.dev/downloads/">kiro.dev/downloads</a>
</div>

<p class="kiro-dim text-sm mt-4">O CLI é opcional, mas recomendado para fluxos de terminal e automações.</p>

</div>
<div>

<img src="/pdf/04-kiro-signin.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Tela inicial do Kiro IDE com o botão Sign in" />
<p class="kiro-dim text-sm text-center mt-2">Após instalar, abra o app — a tela inicial traz o <b>Sign in</b>.</p>

</div>
</div>

<!--
Ao vivo: mostre o site de download e a tela inicial do Kiro recém-instalado.
A autenticação é a Parte 2.
-->

---
layout: center
class: text-center
---

<div class="flex flex-col items-center">
  <span class="kiro-chip mb-6">PARTE 2</span>
  <div class="text-[var(--kiro-purple-light)] mb-4"><KiroMark size="56" /></div>
</div>

# Autenticação & Setup Inicial

<p class="kiro-dim mt-2">Passo 4 — Adicionar o KIRO na IDE via AWS IAM Identity Center</p>

<!--
A autenticação na Hotmart é feita pela organização (AWS IAM Identity Center),
não por Builder ID pessoal. O fluxo tem 6 etapas — vamos uma a uma.
-->

---

# O fluxo de login — visão geral

<div class="grid grid-cols-3 gap-4 mt-6">
  <div class="kiro-card"><span class="kiro-step-num">1</span><div class="mt-2 text-sm">Clicar em <b>Sign in</b> na tela inicial</div></div>
  <div class="kiro-card"><span class="kiro-step-num">2</span><div class="mt-2 text-sm">Escolher <b>Your organization</b></div></div>
  <div class="kiro-card"><span class="kiro-step-num">3</span><div class="mt-2 text-sm"><b>Sign in via IAM Identity Center instead</b></div></div>
  <div class="kiro-card"><span class="kiro-step-num">4</span><div class="mt-2 text-sm">Informar <b>Start URL</b> + <b>Region</b></div></div>
  <div class="kiro-card"><span class="kiro-step-num">5</span><div class="mt-2 text-sm"><b>Permitir acesso</b> na aba do navegador</div></div>
  <div class="kiro-card"><span class="kiro-step-num">6</span><div class="mt-2 text-sm">Confirmar <b>Signed in with AWS IAM Identity Center</b></div></div>
</div>

<p class="kiro-dim text-center text-sm mt-6">Abra um novo link no browser para login durante o processo.</p>

---

# Passos 1 e 2 — Sign in → Your organization

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">1</span>
  <div>Na tela inicial do Kiro, clique em <b>Sign in</b>.</div>
</div>
<div class="flex items-start gap-3">
  <span class="kiro-step-num">2</span>
  <div>Em <i>Choose a way to sign in/sign up</i>, selecione <b class="kiro-accent">Your organization</b> (não Google, GitHub ou Builder ID).</div>
</div>

<div class="kiro-card mt-5 text-sm kiro-dim">
  O login abre uma aba no navegador. Mantenha o Kiro aberto — ele volta a receber o foco ao final.
</div>

</div>
<div>

<img src="/pdf/05-choose-signin.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Tela Choose a way to sign in com Your organization destacado" />

</div>
</div>

---

# Passos 3 e 4 — IAM Identity Center + Start URL

<div class="grid grid-cols-2 gap-6 mt-2">
<div>

<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">3</span>
  <div>Clique em <b class="kiro-accent">Sign in via IAM Identity Center instead</b>.</div>
</div>
<div class="flex items-start gap-3">
  <span class="kiro-step-num">4</span>
  <div>
    Preencha o <b>Start URL</b> e a <b>Region</b>:
    <div class="kiro-card mt-2 text-sm">
      <div><b>Start URL:</b> <code>https://hotmart.awsapps.com/start</code></div>
      <div class="mt-1"><b>Region:</b> <code>us-east-1</code></div>
    </div>
  </div>
</div>

</div>
<div>

<img src="/pdf/06-iam-identity-center-link.png" class="rounded-lg border border-[var(--kiro-border)] w-full mb-3" alt="Link Sign in via IAM Identity Center instead" />
<img src="/pdf/07-start-url-region.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Formulário Start URL e Region" />

</div>
</div>

---

# Passos 5 e 6 — Permitir acesso e confirmar

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">5</span>
  <div>Na aba aberta automaticamente, clique em <b class="kiro-accent">Permitir acesso</b>.</div>
</div>
<div class="flex items-start gap-3 mb-4">
  <span class="kiro-step-num">6</span>
  <div>A IDE já está configurada para uso.</div>
</div>

<div class="kiro-card" style="border-color: var(--kiro-green)">
  ✅ Para conferir, abra a <b>aba do perfil</b> e confirme a mensagem <b class="kiro-accent">“Signed in with AWS IAM Identity Center”</b>.
</div>

</div>
<div>

<img src="/pdf/08-aws-permitir-acesso.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Tela da AWS para permitir que o Kiro IDE acesse os dados" />

</div>
</div>

<!--
Ao vivo: mostre a confirmação no perfil. Reforce: se aparecer "Free Plan", a
configuração está errada — revise (ver próximo slide de erros).
-->

---

# ✅ Checklist Final

<div class="max-w-4xl mx-auto mt-2 kiro-dim">
Seguindo este fluxo, a instalação e a configuração do KIRO ficam padronizadas e alinhadas às diretrizes de segurança e acesso da Hotmart. Antes de iniciar o uso, confirme:
</div>

<div class="grid grid-cols-1 gap-3 mt-6 max-w-4xl mx-auto">
  <div class="kiro-card flex items-center gap-3"><carbon:checkbox-checked class="text-[var(--kiro-green)]" /> Solicitar o acesso ao KIRO pelo <b>IT Service Desk</b>.</div>
  <div class="kiro-card flex items-center gap-3"><carbon:checkbox-checked class="text-[var(--kiro-green)]" /> Verificar no OKTA/AWS se o perfil <b>Amazon-Kiro-Pro-Plus</b> está disponível na conta <b>buildstaging</b>.</div>
  <div class="kiro-card flex items-center gap-3"><carbon:checkbox-checked class="text-[var(--kiro-green)]" /> Instalar e configurar a IDE/CLI conforme as etapas.</div>
  <div class="kiro-card flex items-center gap-3"><carbon:checkbox-checked class="text-[var(--kiro-green)]" /> Confirmar no perfil da IDE a mensagem <b>Signed in with AWS IAM Identity Center</b>.</div>
</div>

---

# ❌ Possíveis erros

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

<div class="kiro-card" style="border-color: var(--kiro-gold)">
  <div class="font-bold" style="color: var(--kiro-gold)">⚠ Atenção: “Free Plan”</div>
  <div class="text-sm kiro-dim mt-1">Se a IDE exibir <b>Free Plan</b>, revise a configuração. Se persistir, acione o suporte responsável.</div>
</div>

<div class="kiro-card mt-4">
  <div class="font-bold">Erro 1 — <code>profileArn is required but could not be resolved</code></div>
  <div class="text-sm kiro-dim mt-2"><b>Causa provável:</b> acesso solicitado recentemente. Mesmo com o perfil já visível na AWS, a liberação pode levar algumas horas.</div>
  <div class="text-sm mt-2"><b class="kiro-accent">Solução:</b> aguarde até <b>24h</b> após a aprovação e tente novamente. Se continuar, acione o suporte.</div>
</div>

</div>
<div>

<img src="/pdf/09-erro-profilearn.png" class="rounded-lg border border-[var(--kiro-border)] w-full" alt="Erro profileArn is required e aviso de Free Plan na IDE" />

</div>
</div>

---
layout: center
class: text-center
---

<div class="flex flex-col items-center">
  <span class="kiro-chip mb-6">PARTE 3</span>
  <div class="text-[var(--kiro-purple-light)] mb-4"><KiroMark size="56" /></div>
</div>

# Ferramentas

<p class="kiro-dim mt-2">Steering · Skills · MCPs · e mais — demonstração</p>

---

# Steering · Skills · Powers · MCPs · Hooks

<table class="w-full text-sm">
<thead>
<tr class="text-left kiro-dim uppercase text-xs tracking-wide">
  <th class="pb-2"></th>
  <th class="pb-2">O que é</th>
  <th class="pb-2">Quando ativa</th>
  <th class="pb-2">Dá ao agente</th>
</tr>
</thead>
<tbody>
<tr class="border-t border-[var(--kiro-border)]">
  <td class="py-3 font-bold flex items-center gap-2"><carbon:compass class="text-[var(--kiro-purple-light)]" /> Steering</td>
  <td class="py-3 kiro-dim">Regras e contexto permanentes do projeto</td>
  <td class="py-3 kiro-dim">Sempre, em toda sessão</td>
  <td class="py-3">Convenções a seguir</td>
</tr>
<tr class="border-t border-[var(--kiro-border)]">
  <td class="py-3 font-bold flex items-center gap-2"><carbon:tools class="text-[var(--kiro-purple-light)]" /> Skills</td>
  <td class="py-3 kiro-dim">Procedimento passo-a-passo para uma tarefa</td>
  <td class="py-3 kiro-dim">Quando referenciada/chamada</td>
  <td class="py-3">Um "como fazer" confiável</td>
</tr>
<tr class="border-t border-[var(--kiro-border)]">
  <td class="py-3 font-bold flex items-center gap-2"><carbon:flash-filled class="text-[var(--kiro-purple-light)]" /> Powers</td>
  <td class="py-3 kiro-dim">Conhecimento especializado de uma tecnologia</td>
  <td class="py-3 kiro-dim">Automático, por palavra-chave</td>
  <td class="py-3">Expertise sob demanda</td>
</tr>
<tr class="border-t border-[var(--kiro-border)]">
  <td class="py-3 font-bold flex items-center gap-2"><carbon:plug class="text-[var(--kiro-purple-light)]" /> MCPs</td>
  <td class="py-3 kiro-dim">Conexão com sistemas e ferramentas externas</td>
  <td class="py-3 kiro-dim">Sempre ativo quando configurado</td>
  <td class="py-3">Novas ações/capacidades reais</td>
</tr>
<tr class="border-t border-[var(--kiro-border)]">
  <td class="py-3 font-bold flex items-center gap-2"><carbon:flash class="text-[var(--kiro-purple-light)]" /> Hooks</td>
  <td class="py-3 kiro-dim">Automação disparada por evento no arquivo</td>
  <td class="py-3 kiro-dim">Ao salvar, criar ou apagar um arquivo</td>
  <td class="py-3">Ação automática em 2º plano</td>
</tr>
</tbody>
</table>

<div class="kiro-card mt-6 text-sm">
  <b class="kiro-accent">Em uma frase:</b> Steering diz <i>quais regras seguir</i>, Skills ensina <i>como fazer uma tarefa</i>, Powers dá <i>conhecimento especializado sob demanda</i>, MCPs conectam o agente a <i>sistemas externos reais</i>, e Hooks disparam <i>ações automáticas por evento</i>.
</div>

<!--
Fecha a Parte 3 amarrando os cinco conceitos. Reforce que eles se complementam:
um MCP conecta ao Neon, um Power ensina a usar bem o Neon, uma Skill define o
passo-a-passo de uma migração, o Steering garante que tudo siga o padrão do
time, e um Hook pode rodar os testes automaticamente a cada save.
-->


---

# Quando usar o Kiro (e quando não)

<div class="grid grid-cols-2 gap-5 mt-3">

<div class="kiro-card !p-4" style="border-color: var(--kiro-green)">
  <div class="flex items-center gap-2 font-bold text-sm" style="color: var(--kiro-green)">
    <carbon:checkmark-filled /> Use o Kiro quando...
  </div>
  <ul class="text-xs kiro-dim mt-2 leading-snug list-disc pl-4 space-y-1">
    <li>Precisa <b>escrever ou alterar código</b></li>
    <li>O fluxo envolve <b>múltiplos arquivos</b> ou etapas</li>
    <li>Quer seguir <b>SDD</b> (requirements → design → tasks)</li>
    <li>Precisa de contexto profundo (steering, specs, histórico)</li>
    <li>Tarefa <b>complexa</b> o suficiente para um agente dedicado</li>
  </ul>
</div>

<div class="kiro-card !p-4" style="border-color: #F15A24; background: rgba(241, 90, 36, 0.08)">
  <div class="flex items-center gap-2 font-bold text-sm" style="color: #F15A24">
    <carbon:chat />
    Use o
    <a
      href="https://chat.hotmart.ai"
      target="_blank"
      class="hover:underline inline-flex items-center gap-1"
      style="color: #F15A24"
    >
      Hotmart Chat <carbon:launch class="text-xs" />
    </a>
    quando...
  </div>
  <ul class="text-xs kiro-dim mt-2 leading-snug list-disc pl-4 space-y-1">
    <li>É uma <b>pergunta pontual</b>, sem gerar código</li>
    <li>Quer <b>consultar dados</b>, schemas, PRs ou tickets</li>
    <li>Quer <b>economizar tokens e contexto</b> do Kiro</li>
    <li>A resposta cabe em uma consulta simples a um MCP</li>
  </ul>
</div>

</div>

<div class="kiro-card !p-4 mt-4">
  <div class="font-bold text-sm mb-1">💬 O Hotmart Chat já vem com vários MCPs prontos</div>
  <div class="kiro-dim text-xs mb-2">Antes de abrir o Kiro para uma pergunta simples, veja se o Chat já resolve:</div>
  <div class="grid grid-cols-5 gap-1.5 text-xs">
    <span class="kiro-chip justify-center !py-1">Golden Path</span>
    <span class="kiro-chip justify-center !py-1">Astrobox</span>
    <span class="kiro-chip justify-center !py-1">Heimdall</span>
    <span class="kiro-chip justify-center !py-1">Heimdall Dados</span>
    <span class="kiro-chip justify-center !py-1">GitHub</span>
    <span class="kiro-chip justify-center !py-1">DataHub</span>
    <span class="kiro-chip justify-center !py-1">Cosmos</span>
    <span class="kiro-chip justify-center !py-1">Astrolens</span>
    <span class="kiro-chip justify-center !py-1">Atlassian</span>
  </div>
</div>

<p class="kiro-dim text-center text-xs mt-3">Regra prática: código → Kiro · consulta rápida → Hotmart Chat</p>

---
layout: center
class: text-center
---

<div class="flex flex-col items-center">
  <span class="kiro-chip mb-6">PARTE 4 · HANDS ON</span>
  <div class="text-[var(--kiro-purple-light)] mb-4"><KiroMark size="56" /></div>
</div>

# Hands On — Spec-Driven Development

<p class="kiro-dim mt-2">Do prompt à spec, da spec ao código</p>

---

# O que é Spec-Driven Development (SDD)

<div class="mt-6 max-w-4xl mx-auto">

O Kiro transforma um **prompt** em artefatos estruturados antes de escrever
código. Em vez de ir direto para a implementação, você acorda com o agente
**o que** será feito e **como**, e só então **executa**.

</div>

<div class="grid grid-cols-3 gap-5 mt-8">
  <div class="kiro-card text-center">
    <carbon:document class="text-3xl text-[var(--kiro-purple-light)] mx-auto" />
    <div class="font-bold mt-2">1. Requirements</div>
    <div class="kiro-dim text-sm">O que precisa ser feito, em requisitos claros.</div>
  </div>
  <div class="kiro-card text-center">
    <carbon:chart-relationship class="text-3xl text-[var(--kiro-purple-light)] mx-auto" />
    <div class="font-bold mt-2">2. Design</div>
    <div class="kiro-dim text-sm">A arquitetura e as decisões técnicas.</div>
  </div>
  <div class="kiro-card text-center">
    <carbon:list-checked class="text-3xl text-[var(--kiro-purple-light)] mx-auto" />
    <div class="font-bold mt-2">3. Tasks</div>
    <div class="kiro-dim text-sm">Tarefas sequenciadas que os agentes executam.</div>
  </div>
</div>

<!--
Explique o porquê: specs reduzem retrabalho, deixam a intenção explícita e
geram código que corresponde ao que foi especificado.
-->

---

# O fluxo de uma spec no Kiro

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

```mermaid {scale: 0.72}
flowchart TD
  A[Prompt inicial] --> B[requirements.md]
  B --> C{Revisar & aprovar}
  C -->|ajustes| B
  C -->|ok| D[design.md]
  D --> E{Revisar & aprovar}
  E -->|ajustes| D
  E -->|ok| F[tasks.md]
  F --> G[Agentes executam tarefas]
  G --> H[Código + testes]
```

</div>
<div>

<div class="kiro-card">

### Arquivos gerados

Cada spec vive em `.kiro/specs/<nome>/`:

- `requirements.md`
- `design.md`
- `tasks.md`

</div>

<div class="kiro-card mt-4">

### A regra de ouro

<b>Revisar cada etapa antes de avançar.</b> A spec é um contrato: aprovar
requirements e design cedo evita retrabalho caro na implementação.

</div>

</div>
</div>

---

# Hands On — vamos fazer juntos

<div class="grid grid-cols-2 gap-8 mt-4">
<div>

### O exercício

Vamos criar uma spec do zero e deixar o agente implementar:

<div class="flex items-start gap-3 mb-3 mt-4">
  <span class="kiro-step-num">1</span>
  <div>Abrir um projeto e iniciar uma <b>nova spec</b>.</div>
</div>
<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">2</span>
  <div>Descrever a feature em um prompt e gerar os <b>requirements</b>.</div>
</div>
<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">3</span>
  <div>Revisar, aprovar e avançar para o <b>design</b>.</div>
</div>
<div class="flex items-start gap-3 mb-3">
  <span class="kiro-step-num">4</span>
  <div>Gerar as <b>tasks</b> e executar com o agente.</div>
</div>
<div class="flex items-start gap-3">
  <span class="kiro-step-num">5</span>
  <div>Revisar o código e os testes gerados.</div>
</div>

</div>
<div>

<div class="kiro-card h-full flex flex-col justify-center">

### Sugestão de feature

Algo pequeno e completo, por exemplo:

<p class="kiro-accent mt-2 font-bold">"Adicionar um endpoint de health check que retorna status e versão da API."</p>

<p class="kiro-dim text-sm mt-4">Simples o bastante para caber no tempo e completo o bastante para passar por requirements, design, tasks, código e testes.</p>

</div>

</div>
</div>

<!--
Mão na massa. Convide a turma a acompanhar no próprio Kiro. Vá devagar nas
aprovações de cada etapa — é o coração do SDD.
-->

---
layout: center
class: text-center
---

<div class="flex flex-col items-center justify-center h-full">
  <div class="text-[var(--kiro-purple-light)] mb-4"><KiroMark size="64" /></div>
  <div class="text-[var(--kiro-text)]"><KiroWordmark :width="240" /></div>

  <div class="mt-8 max-w-2xl">

## Recapitulando

  </div>

  <div class="grid grid-cols-4 gap-3 mt-4 text-sm max-w-4xl">
    <div class="kiro-chip justify-center">1 · Instalação</div>
    <div class="kiro-chip justify-center">2 · Autenticação</div>
    <div class="kiro-chip justify-center">3 · Ferramentas</div>
    <div class="kiro-chip justify-center">4 · SDD</div>
  </div>

  <p class="kiro-dim mt-10">Dúvidas? Vamos abrir o Kiro e explorar juntos.</p>

  <div class="mt-4">
    <a href="https://kiro.dev">kiro.dev</a>
    <span class="kiro-dim mx-2">·</span>
    <a href="https://kiro.dev/docs">Documentação</a>
  </div>
</div>

<!--
Fechamento. Recapitule as 4 partes, abra para perguntas e aponte a documentação
oficial para quem quiser se aprofundar.
-->
