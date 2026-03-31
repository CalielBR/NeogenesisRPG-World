# 📔 Guia de Operação: Neogenesis RPG Page

Este documento serve como manual tático para a edição e expansão da sua página de campanha. Aqui estão as classes CSS e estruturas HTML que garantem o visual Cyberpunk e a responsividade mobile.

---

## 1. Estrutura Base
Toda página deve seguir a estrutura de container para garantir que o conteúdo não encoste nas bordas e funcione via Flexbox:

```html
<div class="container">
    <!-- Seu conteúdo aqui -->
</div>
```

---

## 2. Formatação de Texto
O texto de parágrafos (`<p>`) e listas (`<li>`) já está configurado para ser **justificado** automaticamente.

- **Títulos (H1):** Possuem o efeito *Glitch* automático.
- **Cards:** Use para agrupar blocos de informações ou sessões.
```html
<div class="card">
    <h3>Título do Bloco</h3>
    <p>Conteúdo descritivo.</p>
</div>
```

---

## 3. Calendário e Status
Para a página de Agenda, as cores são baseadas nas classes aplicadas às células (`<td>`):

| Status | Classe | Resultado Visual |
| :--- | :--- | :--- |
| **Confirmado** | `status-scheduled` | Amarelo Cyberpunk 2077 com brilho. |
| **Agendado** | `status-pending` | Branco Giz sólido com brilho suave. |

**Exemplo de uso:**
```html
<tr>
    <td>DATA</td>
    <td>OBJETIVO</td>
    <td class="status-scheduled">CONFIRMADO</td> 
</tr>
<tr>
    <td>DATA</td>
    <td>OBJETIVO</td>
    <td class="status-pending">AGENDADO</td>
</tr>
```

---

## 4. Efeitos Especiais (Visual de Terminal)

### Efeito Typewriter (Máquina de Escrever)
Utilize em textos curtos no topo das páginas. Para linhas sequenciais, adicione um `style="animation-delay: Xs;"`.
```html
<p class="typewriter">> INICIANDO PROTOCOLO...</p>
<p class="typewriter" style="animation-delay: 2.5s;">> CONEXÃO ESTABELECIDA.</p>
```
*Nota: No mobile, a animação é desativada automaticamente para evitar quebra de layout.*

### Citação Arco-Íris (Rainbow Quote)
Para frases de impacto ou profecias:
```html
<div class="rainbow-quote">
    "O futuro é um erro de sistema."
</div>
```

---

## 5. Mídia e Imagens
As imagens utilizam a classe `img-float-right`.

- **No Desktop:** Flutuam à direita com o canto cortado (Cyberpunk style).
- **No Mobile:** Centralizam automaticamente e ocupam a largura da tela.

```html
<img src="caminho/da/imagem.jpg" alt="Descrição" class="img-float-right">
```

---

## 6. Dicas de Manutenção
1. **Links Ativos:** No menu `<nav>`, sempre coloque a classe `class="active"` no link da página onde o usuário está no momento.
2. **Tabelas:** Sempre envolva a `<table>` com uma `<div class="table-wrapper">` para garantir que a tabela tenha rolagem lateral no celular se for muito grande.
3. **Dossiês:** Se criar um personagem novo com cores específicas, use uma classe pai (como `.char-jacques` no CSS) para isolar as cores de títulos.
