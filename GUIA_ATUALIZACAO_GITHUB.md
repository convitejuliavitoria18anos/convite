# Atualização do convite de Júlia Vitória

O pacote foi preparado a partir do ZIP enviado em 27/10/2026. As alterações ficam prontas para você enviar ao GitHub; a publicação acontece quando você atualizar os arquivos do repositório.

## O que foi preparado

1. **Capa para a prévia do link:** `capa-julia-vitoria-v2.jpg`, com 1200 × 630 pixels, “Júlia Vitória”, “18 anos” e “Convite Especial”, no tema tropical.
2. **Aviso de convite individual:** um bloco destacado depois da mensagem de apresentação e um lembrete junto da confirmação.
3. **Localização:** “Povoado Angical” e “Proprietário: Professor Judálio Alencar”, com a busca do mapa complementada pelo nome do povoado.
4. **Calendário:** referência do local complementada e arquivo de calendário com a formatação corrigida.

As oito mídias originais, incluindo fotos, vídeo e áudios, foram preservadas. A data continua em 28/11/2026, às 13h, e a confirmação até 13/11/2026.

## 1. Enviar as alterações prontas para o GitHub

1. Baixe e extraia `Convite_Julia_Vitoria_Atualizado.zip`.
2. Entre no repositório **convitejuliavitoria18anos/conviteespecial**. Use a branch e a pasta configuradas em **Settings → Pages**. A branch principal do repositório é `main`.
3. Abra a pasta `fotos` que já existe no repositório.
4. Clique em **Add file → Upload files** e envie somente `capa-julia-vitoria-v2.jpg`. Salve em **Commit changes**.
5. Volte à pasta onde já está o `index.html`. Envie os quatro arquivos atualizados: `index.html`, `estilo.css`, `convite.js` e `evento.ics`.
6. Salve em **Commit changes** na branch publicada. Se o GitHub abrir uma proposta em outra branch, conclua o pull request e sua integração na branch publicada.
7. Confira em **Actions** se a publicação terminou com sucesso. O GitHub informa que a atualização pode levar até 10 minutos.
8. Abra novamente o convite e confira a capa, o novo aviso e as informações do local.

**Atenção à pasta:** o ZIP contém os arquivos do site diretamente na sua raiz. Envie-os para os mesmos lugares dos arquivos atuais. Não crie uma pasta extra dentro do repositório para colocar o convite.

Não é necessário enviar o ZIP ao GitHub nem reenviar as fotos, o vídeo e os áudios. O arquivo `GUIA_ATUALIZACAO_GITHUB.md` é apenas para consulta.

## 2. Como a nova capa foi configurada

O `index.html` pronto já aponta para a nova imagem no seu domínio do GitHub Pages. O trecho principal é:

```html
<meta property="og:image" content="https://convitejuliavitoria18anos.github.io/conviteespecial/fotos/capa-julia-vitoria-v2.jpg">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
<meta property="og:url" content="https://convitejuliavitoria18anos.github.io/conviteespecial/">
```

O arquivo também inclui título, descrição, texto alternativo e informações para outros tipos de prévia. As referências ao endereço anterior da capa foram substituídas.

**Se quiser mudar somente a capa manualmente:** envie a imagem para `fotos`, abra `index.html`, clique no lápis e substitua a linha antiga de `og:image` e a linha antiga de `og:url` pelas correspondentes acima. Não mantenha duas linhas de `og:image` apontando para capas diferentes. Salve em **Commit changes**.

Após publicar, abra o endereço da imagem no navegador para conferir se ela carrega:

`https://convitejuliavitoria18anos.github.io/conviteespecial/fotos/capa-julia-vitoria-v2.jpg`

Depois, cole o link do convite em uma nova mensagem e aguarde a prévia carregar antes de enviar. O aplicativo pode manter uma prévia anterior em cache. Se isso acontecer, teste uma nova mensagem usando:

`https://convitejuliavitoria18anos.github.io/conviteespecial/?atualizacao=2`

Esse teste não garante a atualização imediata em todos os aplicativos. Limpar o cache do navegador não obriga o WhatsApp a atualizar uma prévia antiga.

## 3. Texto do aviso de convite individual

O bloco destacado no convite contém:

> **Um convite só para você**
>
> **Convite individual · válido para 1 pessoa**
>
> Este convite é exclusivo para o convidado que o recebeu.
>
> Para organizar tudo com carinho e evitar constrangimentos, pedimos que **não compartilhe este link nem leve acompanhantes.**
>
> **Convidado não convida.**
>
> Obrigada pela compreensão e por celebrar comigo!

Perto do formulário de confirmação, foi acrescentado:

> Confirmação individual, exclusiva para quem recebeu o convite.

Para aplicar esse aviso, envie os arquivos `index.html` e `estilo.css` atualizados conforme o passo a passo. O aviso é uma orientação aos convidados; não é um bloqueio técnico de acesso ao link.

## 4. Localização: o que já está pronto

A área do local mostra:

**Piscina Encanto da Natureza**  
**Povoado Angical**  
**Proprietário: Professor Judálio Alencar**

A busca provisória do mapa agora inclui “Piscina Encanto da Natureza Povoado Angical”. Isso acrescenta contexto à pesquisa, mas **ainda não representa um pino exato validado**. O arquivo enviado não traz coordenadas nem um link específico da piscina. Não foi escolhido um ponto no mapa por suposição.

## 5. Substituir a busca pelo pino exato

1. Abra o Google Maps e encontre o ponto correto da piscina. Confirme a entrada com o Professor Judálio Alencar.
2. Abra a ficha desse local ou do pino fixo da entrada.
3. Use **Compartilhar → Copiar link**. Copie o link do local, sem usar compartilhamento de localização em tempo real.
4. No GitHub, abra `convite.js` e clique no lápis. No começo do arquivo, localize `mapa:`.
5. Substitua somente o endereço entre as aspas pelo link que você copiou. Por exemplo, o formato da linha deve ficar assim, com seu link real no lugar da indicação:

```javascript
mapa: 'COLE_AQUI_O_LINK_REAL_DO_PINO'
```

Não salve a indicação acima como se fosse um endereço. Ela serve apenas para mostrar onde colocar seu link.

6. Salve em **Commit changes**.
7. Abra `index.html` e clique no lápis. Procure `id="mapLink"` e substitua somente o endereço do atributo `href` pelo mesmo link real. Isso mantém o destino correto também quando o JavaScript não estiver disponível.
8. Nesse mesmo arquivo, procure a referência ao script e mude sua versão para forçar o carregamento da configuração nova:

```html
<script src="convite.js?v=20261027-2" defer></script>
```

9. Salve em **Commit changes**, aguarde a publicação e teste **Ver localização** no convite. Confira se o destino indicado é a piscina e se o acesso escolhido corresponde à entrada correta.

**Por que alterar dois arquivos?** O botão tem um endereço no HTML, mas o JavaScript o atualiza usando `CONFIG.mapa`. Se você mudar somente o HTML, o endereço antigo do JavaScript poderá voltar a ser usado.

## Referências oficiais

- GitHub: [Adicionar arquivos](https://docs.github.com/pt/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
- GitHub: [Editar arquivos](https://docs.github.com/pt/repositories/working-with-files/managing-files/editing-files)
- GitHub Pages: [Publicação e prazo para refletir alterações](https://docs.github.com/pt/pages/getting-started-with-github-pages/creating-a-github-pages-site)
- Google Maps: [Compartilhar um mapa ou local](https://support.google.com/maps/answer/7101463?hl=pt-BR)
- [Open Graph](https://ogp.me/)

