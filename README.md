# 🏦 PicPay Open Finance Simulator 

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Google Colab](https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252)
![Status](https://img.shields.io/badge/Status-Finalizado-success?style=for-the-badge)

Este projeto simula uma interface bancária de alta fidelidade para o ecossistema **Open Finance**. Desenvolvido inteiramente em Python para ambiente Google Colab, o sistema integra a gestão de crédito, análise de risco global e renegociação de dívidas com persistência de dados em tempo real.

---

## 🚀 Funcionalidades Principais

* **Averbação de Crédito:** Cadastro completo com coleta de dados sensíveis (CPF, Nome da Mãe, Endereço e Renda).
* **Análise de Risco (Open Finance):** O sistema consulta uma API centralizada antes de aprovar qualquer crédito. Se o CPF possuir restrições em QUALQUER banco da rede, a operação é bloqueada automaticamente.
* **Gatilho de Negativação Automática:** Implementação de lógica de tempo real. Se o empréstimo não for quitado até o vencimento, o sistema aplica juros de 30%, reduz o Score para 150 e negativa o cliente na rede global.
* **Score Dinâmico:** Algoritmo que ajusta a reputação financeira do usuário (de 0 a 950) com base no comportamento de pagamento.
* **Portal de Acordos:** Sistema de renegociação que oferece descontos de 30% para liquidação de dívidas, com reabilitação imediata do Score após o pagamento.

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3
* **Interface (UI):** `ipywidgets` com estilização avançada via CSS inline.
* **Comunicação:** `requests` para integração com API REST (Banco Central Centralizado).
* **Data/Hora:** `datetime` para gestão de vencimentos e cálculos de juros.

---

## 📐 Regras de Negócio Implementadas

| Evento | Impacto no Score | Impacto Financeiro |
| :--- | :--- | :--- |
| Contratação | 850 (Incial) | Valor Nominal |
| Atraso (Vencimento) | 150 (Crítico) | +30% de Juros (Multa) |
| Renegociação | 950 (Prime) | -30% de Desconto |
| Quitação | Recuperação Total | Saldo zerado |

---

## 💻 Como Executar

1. Abra o arquivo `.ipynb` deste repositório no **Google Colab**.
2. Certifique-se de que a URL do Banco Central está ativa no código.
3. Execute todas as células.
4. Utilize a interface gráfica gerada no final do notebook para interagir com o banco.

---

## 🧑‍💻 Autor

Desenvolvido como projeto de simulação de sistemas bancários e integração de dados.
