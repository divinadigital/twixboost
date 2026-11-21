# TwixBoost

Otimizador do Windows para jogos. Cada ajuste pede confirmação, guarda o valor original e pode ser desfeito com um clique. Tudo roda no seu PC: nada é enviado para a internet.

## Baixar

**[Baixar o instalador do TwixBoost](https://github.com/divinadigital/twixboost/releases/latest/download/TwixBoost-Setup.exe)** (cerca de 31 MB)

Funciona no Windows 10 e 11, 64 bits. Notas de cada versão em [Releases](https://github.com/divinadigital/twixboost/releases).

O TwixBoost abre como administrador, porque ajusta configurações do sistema: o Windows pede o seu "Sim" sempre que ele abre. Na instalação, a opção "Abrir o TwixBoost quando o Windows iniciar" faz ele começar junto com o PC, já perto do relógio e sem pedir o "Sim". Só uma cópia fica aberta por vez; abrir de novo traz a janela que já está aberta.

### Aviso "O Windows protegeu o computador"

O instalador não tem assinatura digital paga, então o Windows pode mostrar esse aviso azul na primeira vez. Clique em **Mais informações** e depois em **Executar assim mesmo**.

Para conferir se o arquivo é o original, rode no PowerShell, na pasta do download, e compare com o SHA-256 da página da versão:

```powershell
Get-FileHash .\TwixBoost-Setup.exe
```

## O que ele faz

- **Modo Jogo**: com um clique, coloca o plano de energia em desempenho, fecha os programas da sua lista e dá prioridade alta ao jogo. "Sair do Modo Jogo" desfaz tudo. Quando um jogo abre, o TwixBoost identifica qual é e sugere ativar o Modo Jogo para ele.
- **Perto do relógio**: fechar a janela deixa o TwixBoost na área de notificação, avisando quando um jogo abre e quando a bateria de um periférico fica fraca. Para encerrar, clique com o botão direito no ícone e escolha "Fechar o TwixBoost".
- **Limpeza**: um clique limpa arquivos temporários, cache de shaders e lixeira, só o que tiver algo, com o progresso num anel em volta da vassoura. Antes de apagar, mostra quanto vai liberar de cada parte.
- **Energia**: planos Alto desempenho e Ultimate Performance, com volta ao plano que você usava.
- **Serviços**: desativa serviços de segundo plano da lista, cada um com restauração.
- **Rede**: limite de rede multimídia, CPU reservada ao fundo, limpeza do cache DNS e reset do Winsock.
- **Sistema**: Modo de Jogo do Windows, agendamento de GPU, inicialização rápida, hibernação, Xbox Game Bar e gravação em segundo plano.
- **Diagnóstico**: relatório do hardware e das configurações, salvo num arquivo .txt.
- **Periféricos**: mostra o modelo do mouse, do teclado e do fone e a bateria dos que informam a carga: Logitech (Lightspeed, Unifying e Bolt), Astro A50 de 4ª geração, Redragon Sniper Pro e aparelhos Bluetooth, sem precisar do programa do fabricante aberto. Com 20% ou menos, manda uma notificação do Windows perto do relógio pedindo para carregar o aparelho.

## O que ele nunca faz

- Desativar ou alterar antivírus, Windows Defender, firewall ou atualizações de segurança.
- Mexer em anti-cheat ou em arquivos dentro das pastas dos jogos.
- Enviar dados para a internet.
- Fechar processos do sistema ou que não estejam na sua lista.

Antes da primeira otimização, ele tenta criar um ponto de restauração do Windows. O botão **Desfazer tudo** reverte as mudanças, da mais recente para a mais antiga.

## Desinstalar

Se quiser voltar o Windows ao que era, abra o TwixBoost e use **Desfazer tudo** antes. Depois remova em **Configurações > Aplicativos > Aplicativos instalados > TwixBoost**.

Os valores originais e os logs ficam em `%LOCALAPPDATA%\TwixBoost`. Apague essa pasta se não for reinstalar.
