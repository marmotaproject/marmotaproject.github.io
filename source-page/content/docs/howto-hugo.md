---
title: "Como enviar um PR para o projeto"
date: 2020-05-08T20:53:54-03:00
draft: false
---

Se você deseja contribuir para a página do projeto marmota e não sabe como, abaixo tem o passo a passo:

* Instale o Golang em seu pc/laptop. 
Se for alguma distro Linux, basta digita este comando:
```bash
curl -s https://raw.githubusercontent.com/lobocode/gotools/master/goinstall/goinstall.sh | bash
```
Caso seja Windows ou Mac, consulte a **[documentação oficial](https://golang.org/dl/)**.
* Em seguida, **[instale o Hugo](https://gohugo.io/getting-started/installing/)**.
* Faça um fork do projeto e em seguida clone ele em sua máquina com o seguinte comando:
```bash
git clone https://github.com/seuUsuario/marmotaproject.github.io/
```

* Com o projeto em sua máquina, com o Go e o Hugo instalados, entre na pasta do projeto e em seguida na pasta `source-page`:
```bash
~/ cd marmotaproject.github.io/source-page
```

* A pasta `source-page` contém o código fonte da página. Isto é, para editar, adicionar, remover qualquer conteúdo e\ou modificar a estrutura da pagina, você deverá manipular os arquivos desta pasta. Por exemplo:
    Para adicionar um novo post, digite `hug new post/novopost.md`, e teste com o comando `hugo server` que irá lhe retornar uma url local `http://localhost:1313`. Da mesma forma se você desejar editar algum link do menu, basta editar os arquivos contidos na pasta `content/page/tutoriais.md` por exemplo. 

* Com a edição feita, digite `hugo -d ../`. Assim a estrutura da página estática em html/css/js, será gerado na pasta do projeto. Isto é, na pasta `marmotaproject.github.io`.
* Após as mudanças serem feitas, envie um `git pull` para seu fork e em seguida um `Pull Request` das modificações para o projeto oficial para que seja feito um Merge.

> **Nota**: Cuidado para não gerar a página estática no mesmo diretório do `source-page`. Assim você evita sobrescrita de arquivos o que pode gerar confusão.
