# 🌐 ConnectMix

Bem-vindo ao repositório oficial da **ConnectMix**! 🚀  
Aqui centralizamos os projetos mais importantes que impulsionam nossas operações internas, APIs, e integrações.  
Este documento também servirá como guia para o uso do **Git**, **Git Flow**, e as **GitHub Actions** adotadas por nossa organização.

---

## 📌 Organização Interna

### 🎯 Nosso Sistema Principal: **infra**
O repositório **infra** é o núcleo do sistema interno da ConnectMix, responsável por gerenciar e sustentar os processos críticos da organização.

### 🌟 Outros Repositórios Relevantes
Além do sistema principal, possuímos diversos repositórios que abrangem APIs, integrações e ferramentas internas, como:
- **api-infra**  
- **api-ads**  
- **api-whatsapp**  
- **queue-service**  
- E outros mais.  

**Nota**: Todos os repositórios são privados e desenvolvidos majoritariamente em PHP, TypeScript e JavaScript.

---

## 🛠️ Como Trabalhamos com Git

### 📖 Padrões de Uso
Utilizamos o Git para versionamento de código de forma colaborativa e organizada. Seguem os principais pontos para trabalhar conosco:
  
#### 1. **Clone do Repositório**  
  ```bash
  git clone <URL_DO_REPOSITORIO>
  cd <PASTA_DO_REPOSITORIO>
```
   
#### 2.  **Criação de Branches**
Trabalhamos com Git Flow (detalhes abaixo), então branches são essenciais:

  ```bash
  git checkout -b feature/nome-da-feature
  ```

#### 3.  **Commits Semânticos**
Mantenha as mensagens de commit claras e padronizadas:

  ```bash
  git commit -m "feat: descrição da funcionalidade"
  ```

**Exemplo de Prefixos:**

- `feat:` para novas funcionalidades
- `fix:` para correções de bugs
- `docs:` para alterações na documentação
- `refactor:` para refatorações de código

#### 4. **Envio de Alterações**

  ```bash
  git push origin <nome-da-branch>
  ```

#### 5. **Pull Requests**
Após concluir uma task, abra um Pull Request (PR) no GitHub para revisão.

---

## 🌀 Fluxo de Trabalho com Git Flow
Adotamos o **Git Flow** para garantir um fluxo de trabalho organizado e eficiente:

- **Main**: Branch principal, pronta para produção.  
- **Develop**: Branch de integração, onde as features são testadas antes de irem para produção.  
- **Feature**: Usada para desenvolver novas funcionalidades. Criada a partir da develop.  
- **Release**: Usada para preparar uma nova versão.  
- **Hotfix**: Para correções urgentes na main.

### 📝 Exemplo de Fluxo:
1. Criar uma nova feature:

   ```bash
   git checkout develop  
   git checkout -b feature/nova-funcionalidade
   ```

3. Desenvolver e enviar mudanças:

   ```bash
   git add .  
   git commit -m "feat: nova funcionalidade implementada"  
   git push origin feature/nova-funcionalidade
   ```

5. Abrir PR e integrar na develop.

6. Após testes, integrar na main via branch de release.

---

## ⚙️ GitHub Actions

Utilizamos **GitHub Actions** para automatizar nossos fluxos de trabalho.

### 🌐 Deploys Automatizados

- **Branch Develop**:  
  Cada merge na branch develop dispara um deploy para o ambiente de **Homologação**.  
  Os serviços são acessíveis pelos domínios:  
  *.connectmix.dev  

- **Branch Main (ou Master)**:  
  Cada criação de **tag** de versão na branch main (ou master) deve ter o formato `v***` e dispara um deploy para o ambiente de **Produção**.

---

## 🧩 Contribuindo com os Projetos

1. Verifique a documentação do repositório específico.  
2. Crie uma issue detalhada para discutir a mudança ou correção.  
3. Utilize branches de feature para qualquer desenvolvimento.  
4. Sempre abra um Pull Request e aguarde a aprovação antes de fazer merge.

---

## 📞 Contato

Se precisar de ajuda, entre em contato com nossa equipe:  
- **Email**: gabriel@gabrielstringari.com
- **WhatsApp**: Grupo de whatsapp  
- **Discord**: Canal interno #desenvolvimento 

🌟 **Obrigado por colaborar com a ConnectMix!** 🌟
