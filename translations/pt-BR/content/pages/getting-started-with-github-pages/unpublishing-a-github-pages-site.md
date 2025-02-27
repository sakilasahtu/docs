---
title: Cancelar a publicação de um site do GitHub Pages
intro: 'Você pode cancelar a publicação do seu site de {% data variables.product.prodname_pages %} para que não fique mais disponível.'
redirect_from:
  - /articles/how-do-i-unpublish-a-project-page
  - /articles/unpublishing-a-project-page
  - /articles/unpublishing-a-project-pages-site
  - /articles/unpublishing-a-user-pages-site
  - /articles/unpublishing-a-github-pages-site
  - /github/working-with-github-pages/unpublishing-a-github-pages-site
product: '{% data reusables.gated-features.pages %}'
permissions: 'People with admin or maintainer permissions for a repository can unpublish a {% data variables.product.prodname_pages %} site.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pages
shortTitle: Cancelar a publicação do site de páginas
---

{% ifversion pages-custom-workflow %}

Quando você cancelar a publicação de seu site, o site não estará mais disponível. Todas as configurações de repositório ou o conteúdo não serão afetados.

{% data reusables.repositories.navigate-to-repo %}
1. Em **{% data variables.product.prodname_pages %}**, ao lado da mensagem **seu site está ativo em**, clique em {% octicon "kebab-horizontal" aria-label="the horizontal kebab icon" %}.
1. No menu que será exibido, selecione **Cancelar a publicação do site**.

   ![Menu suspenso para cancelar a publicação do site](/assets/images/help/pages/unpublish-site.png)

{% else %}

## Cancelar a publicação de um site de projeto

{% data reusables.repositories.navigate-to-repo %}
2. Se existir um branch `gh-pages` no repositório, exclua o branch `gh-pages`. Para obter mais informações, consulte "[Criar e excluir branches em seu repositório](/articles/creating-and-deleting-branches-within-your-repository#deleting-a-branch)".
3. Se o branch `gh-pages` fosse a sua fonte de publicação, {% ifversion fpt or ghec %}pule para a etapa 6{% else %}agora o seu site não está publicado e você pode pular as etapas restantes{% endif %}.
{% data reusables.repositories.sidebar-settings %}
{% data reusables.pages.sidebar-pages %}
5. No "{% data variables.product.prodname_pages %}", use o menu suspenso **Source** (Fonte) e selecione **None** (Nenhuma). ![Menu suspenso para selecionar uma fonte de publicação](/assets/images/help/pages/publishing-source-drop-down.png)
{% data reusables.pages.update_your_dns_settings %}

## Cancelar a publicação de um site de usuário ou organização

{% data reusables.repositories.navigate-to-repo %}
2. Exclua o branch que você está usando como fonte de publicação ou exclua todo o repositório. Para obter mais informações, consulte "[Criar e excluir branches no repositório](/articles/creating-and-deleting-branches-within-your-repository#deleting-a-branch)" e "[Excluir um repositório](/articles/deleting-a-repository)".
{% data reusables.pages.update_your_dns_settings %}

{% endif %}
