No ecossistema de desenvolvimento **AI-Native**, o fluxo de trabalho abandona a codificação isolada para adotar uma **estrutura multi-agente encadeada**. Nessa arquitetura, o processo é dividido em duplas funcionais: para cada fase, existe um **Agente Gerador** (responsável pela criação e execução) emparelhado com um **Agente de QA/Checksum** (responsável por auditar, testar e verificar segurança e qualidade). Os especialistas humanos atuam como **validadores finais** em cada etapa do ciclo V-Bounce.

Abaixo está a sequência completa dos **12 sub-agentes** organizada por fases, com destaque para os **pontos de verificação de segurança**:

---

### **Fase 1: Planejamento & Definição de Escopo**
* **Agent-01 (Project Planning Agent):** Recebe as intenções do produto em linguagem natural, define os objetivos gerais, estima cronogramas e mapeia os recursos necessários.
* **Agent-02 (Planning QA Agent):** Avalia a viabilidade do plano, identifica gargalos operacionais e analisa os riscos preliminares de infraestrutura e alocação.

---

### **Fase 2: Engenharia de Requisitos & Critérios de Aceitação**
* **Agent-03 (Requirement Engineering Agent):** Decompõe os objetivos de alto nível em requisitos funcionais e não funcionais detalhados, construindo matrizes de rastreabilidade automática.
* **Agent-04 (Requirement QA Agent):** Analisa ambiguidades nas especificações e define os **requisitos de conformidade de dados, privacidade e limites de aceitação probabilísticos (*Evals*)**.

---

### **Fase 3: Design, Arquitetura & Modelagem de Ameaças**
* **Agent-05 (System & Architecture Designer):** Gera diagramas de sistema (UML, microserviços), esquemas de banco de dados e contratos de APIs e de dados.
* **Agent-06 (Design & Security QA Agent):** Realiza a **modelagem de ameaças (*Threat Modeling*)**, analisa a superfície de ataque da arquitetura planejada e emite recomendações de segurança modular antes de qualquer código ser escrito.

---

### **Fase 4: Testes Contínuos & Cobertura (V-Bounce)**
* **Agent-07 (Software Tester Agent):** Cria em tempo real suítes de testes unitários, testes de integração e cenários de borda (*edge cases*) alinhados diretamente aos requisitos definidos.
* **Agent-08 (Testing QA Agent):** Avalia a cobertura de código, executa testes de mutação e projeta simulações de carga, estresse e resiliência do sistema.

---

### **Fase 5: Desenvolvimento & Verificação Estrita de Segurança (Coding)**
* **Agent-09 (Code Developer Agent):** Escreve o código-fonte da aplicação, pipelines de dados e scripts de automação em velocidade quase instantânea.
* **Agent-10 (Code QA & Security Verification Agent):** É o principal guardião de segurança no código. Ele executa:
  * **Análise Estática de Segurança (SAST):** Varredura automática em busca de vulnerabilidades (como injeções SQL, XSS, estouro de buffer e credenciais expostas).
  * **Análise de Dependências:** Verificação de pacotes externos em busca de vulnerabilidades conhecidas (CVEs).
  * **Otimização de Segurança em Tempo Real:** Refatoração de trechos inseguros ou ineficientes.

---

### **Fase 6: Implantação, CI/CD & Governança em Tempo de Execução**
* **Agent-11 (Deployment Plan Agent):** Elabora scripts de *Infrastructure as Code* (IaC), pipelines de CI/CD e estratégias de implantação progressiva (*canary* ou *shadow deployments*).
* **Agent-12 (Deployment & Runtime QA Agent):** Atua no ambiente final aplicando **Governança como Código**:
  * Valida políticas de controle de acesso e permissões de produção.
  * Varre vulnerabilidades no ambiente de implantação e gera automaticamente a documentação de auditoria (*Model Cards* e *Datasheets*).
  * Monitora o comportamento do sistema em tempo de execução para barrar injeções de prompt ou desvios (*drift*).

---

### 🛡️ O Papel da Validação Humana (Human-in-the-Loop)
Nenhuma transição entre fases ocorre de forma 100% autônoma para componentes críticos. O time humano de validação (*Dev & PM Validators*) recebe os relatórios consolidados dos agentes de QA (como o **Agent-10** na segurança do código) para dar o aceite final (*Approval*) e avançar para a próxima etapa.

---

🔍 Se quiser, posso detalhar os testes específicos de segurança que o **Agent-10** utiliza para validar vulnerabilidades em código gerado por IA.
