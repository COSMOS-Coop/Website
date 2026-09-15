 <div align="center">
   <img width="256" height="256" alt="logo_DARK_CLEAN" src="https://github.com/user-attachments/assets/c119df40-bed2-42e0-9ce6-a53d74b6b5df" />
   <p><h3>The Website</h3></p>
   <p>Nosso portfólio e portal de inscrição.</p>
 </div>

---

### Arquitetura

- `/frontend`:
  - Nossa **landing page**, contem uma introdução ao COSMOS, link para o nosso manifesto, nossos projetos e link para o formulário inscrição.
  - Deploy é feito usando o cloudflare pages.
  - `/page/inscreva-se/` é nosso **forms de inscrição**, manda o post request pro `/worker` a cada nova inscrição.
- `/worker`:
  - Uma serverless function que notifica o servidor do COSMOS quando uma inscrição acontece para os membros atuais poderem incluir o membro novo.
  - Usa cloudflare workers junto a webhooks para mandar mensagens pro discord.
- `/misc`:
  - dados adicionais, documentações e afins.
 
### Tarefas

- [ ] Esqueleto do projeto
- [ ] Configurar deploy do pages
- [ ] Configurar deploy do worker
- [ ] Mockup da landing page
- [ ] Mockup do forms de inscrição
- [ ] Definir API para comunicação com o worker
- [ ] Configurar webhook entre o worker e o discord
