$ echo "# github_pages" >> README.md
$ git init
git add README.md
git commit -m "first commit"

adding origin or updating it

git remote add origin ssh://github.com-work_user1/saapra/github_pages.git
OR
git remote set-url ssh://github.com-work_user1/saapra/github_pages.git


NOW HOW TO make this working ?

$ ssh-keygen -t rsa   <= makes new public and priv key
   ~/.ssh/id_rsa and ~/.ssh/id_rsa.pub

Take pub key and add to github
Take private key and add to ~/.ssh/config like:

Host github.com-work_user1
   HostName github.com
   User git
   IdentityFile ~/.ssh/id_rsa


and thats how ssh://github.com-work_user1/saapra/github_pages.git starts working

from then git push and stuff works fine