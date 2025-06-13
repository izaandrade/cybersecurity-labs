# 🛡️ Offensive Security Intro — Your First Hack  

**Plataforma:** TryHackMe  
**Dificuldade:** Iniciante  
**Data:** 13/06/2025  

---

## 📝 Descrição  

Essa atividade prática introduz o conceito de **Brute-Force de diretórios** utilizando a ferramenta **Gobuster**, para localizar páginas ocultas em um site vulnerável fictício chamado *FakeBank*.  
O objetivo foi localizar páginas administrativas escondidas e simular um ataque de transferência bancária não autorizada.

---

## 📌 Objetivos  

- Entender o conceito de brute-force de diretórios
- Aprender a usar o **Gobuster** para encontrar páginas escondidas
- Simular a exploração de uma falha de segurança  
- Realizar uma transferência de dinheiro no ambiente controlado

---

## 🔧 Ferramentas Utilizadas  

- Terminal Linux  
- [Gobuster](https://github.com/OJ/gobuster)  

---

## 🛠️ Procedimento  

**1️⃣ Abertura do Terminal**  
Iniciei o terminal no ambiente da TryHackMe.

**2️⃣ Execução do Gobuster**  
Utilizei o seguinte comando para forçar diretórios no site `http://fakebank.thm`:
gobuster -u http://fakebank.thm -w wordlist.txt dir


**Parâmetros:**  
- `-u` → URL alvo  
- `-w` → wordlist de palavras possíveis para páginas/diretórios  
- `dir` → modo de brute-force para diretórios  

**Resultado:**  
/images (Status: 301)
/bank-transfer (Status: 200)


**3️⃣ Exploração da Página Oculta**  
Acesseio `http://fakebank.thm/bank-transfer` no navegador.  
Na interface de transferência, realizei a operação:

- Transferir **$2000** da conta **2276** para minha conta **8881**

**4️⃣ Verificação da Transferência**  
Acessei a página de saldo da conta e confirmei a alteração no saldo após a transação.

---

## 📚 Conceitos Aprendidos  

- Como realizar brute-force de diretórios e arquivos web  
- Diferença de status codes HTTP (200 = OK, 301 = redirect etc.)  
- Como páginas mal protegidas podem expor funções críticas  
- Ética na atuação de segurança ofensiva: identificar e relatar falhas de forma responsável  

---

## ✅ Conclusão  

Primeiro lab prático executado com sucesso!  
Foi excelente para entender na prática como páginas ocultas podem comprometer sistemas, e como ferramentas como o **Gobuster** podem ajudar a identificá-las. Um exemplo simples, mas muito didático, de como falhas de configuração podem ser exploradas.

---

## 📎 Referência  

- [TryHackMe — Offensive Security Intro](https://tryhackme.com/room/offensivesecurityintro)

