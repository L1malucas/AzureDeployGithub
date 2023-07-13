# CI/CD Deploy no Azure com Github

Repositório de referência para desenvolvedores iniciantes, conseguirem rapidamente executar deploy no Azure a partir de um repositório Git e manter o deploy atualizado com a branch **Main** em QUATRO passos!


1. **Criando Web App no Azure**
   1. Dentro do setup de criação do azure web app, selecione:
   2. O **resource group** que será usado;
   3. Logo abaixo escolha o **nome** da aplicação;
   4. Defina a **runtime stack** de sua escolha e lembre-se de usar a **MESMA VERSÃO!** quando criar o projeto;
   5. Selecione o sistema operacional **linux** e o **pricing plan** de sua escolha;
   6. Clique em **Review + Create**;
   7. Após criado, navegue até o recurso e faça download do **publish profile**;
2. **Hora do Código!**
   1. Desenvolva seu projeto e faça upload no github;
3. **Github Secret e Actions**
   1. Acesse as configurações do seu projeto hospedado no **github** em: *settings/secrets and variables/actions*;
   2. Crie uma nova **New Repository Secret**, defina um nome para sua secret, cole o código do **publish profile** no campo abaixo do nome e salve;
   3. Copie o arquivo **CI/CD** desse repositório;
   4. Navegue até a aba **Actions** do github no seu projeto, selecione a opção **set up a workflow yourself** e cole o código copiado no passo anterior; 
   5. Altere o valor da *env*  **AZURE_WEBAPP_NAME** para o mesmo nome que foi criado o web app no azure (passo 1.iii);
   6. Substitua o nome da solução nas linhas **26, 29, 32**, para o nome da sua própria solução;
4. **Commit e mágica**
   1. Após alterações realizadas, faça **commit** e veja mágica acontecer
