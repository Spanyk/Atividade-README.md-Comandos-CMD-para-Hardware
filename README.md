<div align="center" >


# 🖥️ Guia de Comandos Úteis do Windows

[<img src="https://avatars.githubusercontent.com/u/90398620?v=4" width=115 > <br> <sub> Paulo Peixoto </sub>](https://github.com/Spanyk) |
| :---: |  

**Manutenção de Hardware, Redes e Sistema Operacional**

![Autor](https://img.shields.io/badge/Autor-Spanyk%20-blue)
![Data](https://img.shields.io/badge/Data-19/09/2025%20-red)
![Github](https://img.shields.io/badge/Github-Spanyk%20-purple)

</div>

```
🧠 O que aprendi?
Com esta atividade aprendi a criar e editar arquivos README.md, registrar informações de projetos e documentar comandos úteis do CMD voltados para manutenção de hardware. 
Também aprendi a organizar informações de forma clara e compartilhá-las em um repositório GitHub.

```


<br>

## 🛠️ Diagnóstico e Manutenção do Sistema

| ⚙️ Comando                                                                | 📝 Descrição                           | 💡 Exemplo / Como executar                                                             |
| ------------------------------------------------------------------------- | -------------------------------------- | -------------------------------------------------------------------------------------- |
| `MDSCHED`                                                                 | Diagnóstico de memória RAM             | Executar → digitar `MDSCHED` → reiniciar computador para testar RAM (Admin necessário) |
| `MSDT`                                                                    | Suporte e diagnóstico Microsoft        | CMD ou Executar → `MSDT` → seguir assistente (Admin recomendado)                       |
| `SFC /SCANNOW`                                                            | Verifica e repara arquivos de sistema  | CMD (Admin) → `sfc /scannow`                                                           |
| `SFC /VERIFYONLY`                                                         | Apenas verifica integridade do sistema | CMD (Admin) → `sfc /verifyonly`                                                        |
| `SFC /SCANFILE=arquivo`                                                   | Verifica/repara arquivo específico     | CMD (Admin) → `sfc /scanfile=C:\Windows\System32\kernel32.dll`                         |
| `DISM /Online /Cleanup-Image /RestoreHealth`                              | Repara arquivos do sistema online      | CMD (Admin) → `DISM /Online /Cleanup-Image /RestoreHealth`                             |
| `DISM /Image:C:\offline /Cleanup-Image /RestoreHealth /Source:C:\Windows` | Repara uma imagem offline              | CMD (Admin) → substituir caminho da imagem                                             |
| `VERIFIER`                                                                | Testa estabilidade de drivers          | CMD (Admin) → `verifier`                                                               |
| `MSCONFIG`                                                                | Gerencia inicialização e serviços      | Executar → `msconfig` → aba Inicialização                                              |
| `GET-PHYSICALDISK`                                                        | Info de discos físicos                 | PowerShell (Admin) → `Get-PhysicalDisk`                                                |
| `wmic diskdrive get caption,status`                                       | Detecta falhas em discos               | CMD (Admin) → `wmic diskdrive get caption,status`                                      |
| `winget upgrade --all`                                                    | Atualiza programas                     | CMD (Admin) → `winget upgrade --all`                                                   |
| `gpresult /r`                                                             | Exibe políticas de grupo               | CMD (Admin recomendado) → `gpresult /r`                                                |
| `SYSTEMINFO`                                                              | Info detalhada de hardware e OS        | CMD ou Executar → `systeminfo`                                                         |
| `DXDIAG`                                                                  | Diagnóstico DirectX                    | Executar → `dxdiag`                                                                    |
| `EVENTVWR.MSC`                                                            | Visualizador de eventos                | Executar → `eventvwr.msc`                                                              |

---

## 💾 Administração e Diagnóstico de Discos

| 💽 Comando     | 📝 Descrição                        | 💡 Exemplo / Como executar                  |
| -------------- | ----------------------------------- | ------------------------------------------- |
| `CHKDSK`       | Verifica integridade do disco       | CMD (Admin) → `chkdsk C: /F /R`             |
| `CLEANMGR`     | Limpeza de disco                    | Executar → `cleanmgr` → selecionar unidade  |
| `DEFRAG`       | Desfragmenta discos                 | CMD (Admin) → `defrag C: /O`                |
| `DISKMGMT.MSC` | Gerenciamento de discos             | Executar → `diskmgmt.msc`                   |
| `DISKPART`     | Gerenciamento avançado de partições | CMD (Admin) → `diskpart` → `list disk`      |
| `FORMAT`       | Formata unidade                     | CMD (Admin) → `format D: /FS:NTFS`          |
| `XCOPY`        | Copia arquivos e pastas             | CMD → `xcopy C:\origem D:\destino /E /H /C` |

---

## 🌐 Rede e Internet

| 🌐 Comando                            | 📝 Descrição                       | 💡 Exemplo / Como executar                     |
| ------------------------------------- | ---------------------------------- | ---------------------------------------------- |
| `IPCONFIG`                            | Info básica de rede                | CMD → `ipconfig`                               |
| `IPCONFIG /ALL`                       | Info detalhada de todas interfaces | CMD → `ipconfig /all`                          |
| `IPCONFIG /RELEASE`                   | Libera IP atual                    | CMD → `ipconfig /release` (Admin recomendado)  |
| `IPCONFIG /RENEW`                     | Renova IP                          | CMD → `ipconfig /renew` (Admin recomendado)    |
| `IPCONFIG /FLUSHDNS`                  | Limpa cache DNS                    | CMD → `ipconfig /flushdns` (Admin recomendado) |
| `IPCONFIG /DISPLAYDNS`                | Mostra cache DNS                   | CMD → `ipconfig /displaydns`                   |
| `PING [host]`                         | Testa conectividade                | CMD → `ping google.com`                        |
| `TRACERT [host]`                      | Mostra rota dos pacotes            | CMD → `tracert google.com`                     |
| `PATHPING [host]`                     | Diagnóstico avançado de rota       | CMD → `pathping google.com`                    |
| `NETSTAT`                             | Conexões e portas ativas           | CMD → `netstat -an`                            |
| `CONTROL NETCONNECTIONS` / `NCPA.CPL` | Conexões de rede                   | Executar → `ncpa.cpl`                          |
| `FIREWALL.CPL`                        | Firewall do Windows                | Executar → `firewall.cpl`                      |
| `WF.MSC`                              | Firewall Avançado                  | Executar → `wf.msc`                            |
| `INETCPL.CPL`                         | Propriedades da Internet           | Executar → `inetcpl.cpl`                       |

---

## 📂 Arquivos e Diretórios

| 📂 Comando                  | 📝 Descrição            | 💡 Exemplo / Como executar            |
| --------------------------- | ----------------------- | ------------------------------------- |
| `CD [caminho]`              | Navega entre diretórios | CMD → `cd C:\Windows\System32`        |
| `DIR`                       | Lista arquivos e pastas | CMD → `dir`                           |
| `MKDIR [nome]`              | Cria pasta              | CMD → `mkdir C:\NovaPasta`            |
| `DEL [arquivo]`             | Exclui arquivo          | CMD → `del C:\arquivo.txt`            |
| `COPY [origem] [destino]`   | Copia arquivos          | CMD → `copy C:\arquivo.txt D:\Backup` |
| `REN [arquivo] [novo_nome]` | Renomeia arquivo        | CMD → `ren arquivo.txt novo.txt`      |
| `TYPE [arquivo]`            | Mostra conteúdo         | CMD → `type C:\arquivo.txt`           |
| `ATTRIB [arquivo]`          | Mostra/Altera atributos | CMD → `attrib +R C:\arquivo.txt`      |
| `FIND "texto" [arquivo]`    | Procura texto           | CMD → `find "erro" C:\log.txt`        |
| `CIPHER`                    | Criptografia NTFS       | CMD → `cipher /E C:\Docs`             |

---

## 🖱️ Painel de Controle e Ferramentas do Sistema

| 🛠️ Comando                           | 📝 Descrição                      | 💡 Exemplo / Como executar                                  |
| ------------------------------------- | --------------------------------- | ----------------------------------------------------------- |
| `APPWIZ.CPL`                          | Adicionar/Remover Programas       | Executar → `appwiz.cpl`                                     |
| `CERTMGR.MSC`                         | Certificados do usuário atual     | Executar → `certmgr.msc`                                    |
| `COMPMGMT.MSC`                        | Gerenciamento do computador       | Executar → `compmgmt.msc`                                   |
| `CONTROL`                             | Painel de Controle                | Executar → `control`                                        |
| `CONTROL ADMINTOOLS`                  | Ferramentas Administrativas       | Executar → `control admintools`                             |
| `CONTROL FOLDERS`                     | Opções de pasta                   | Executar → `control folders`                                |
| `CONTROL FONTS`                       | Gerenciador de fontes             | Executar → `control fonts`                                  |
| `CONTROL KEYBOARD`                    | Configurações do teclado          | Executar → `control keyboard`                               |
| `CONTROL MOUSE` / `MAIN.CPL`          | Configurações do mouse            | Executar → `control mouse`                                  |
| `CONTROL PRINTERS`                    | Impressoras e fax                 | Executar → `control printers`                               |
| `CONTROL USERPASSWORDS2` / `NETPLWIZ` | Gerenciar usuários e senhas       | Executar → `netplwiz` (Admin recomendado)                   |
| `DEVMGMT.MSC`                         | Gerenciador de dispositivos       | Executar → `devmgmt.msc` (Admin recomendado)                |
| `GPEDIT.MSC`                          | Editor de políticas de grupo      | Executar → `gpedit.msc` (Admin recomendado, Pro/Enterprise) |
| `LUSRMGR.MSC`                         | Usuários e grupos locais          | Executar → `lusrmgr.msc` (Admin)                            |
| `MSCONFIG`                            | Configuração de inicialização     | Executar → `msconfig`                                       |
| `MSINFO32`                            | Informações detalhadas do sistema | Executar → `msinfo32`                                       |
| `REGEDIT` / `REGEDT32`                | Editor do registro                | Executar → `regedit` (Admin)                                |
| `SERVICES.MSC`                        | Gerenciar serviços do Windows     | Executar → `services.msc` (Admin recomendado)               |
| `SYSDM.CPL`                           | Propriedades do sistema           | Executar → `sysdm.cpl`                                      |
| `TASKMGR`                             | Gerenciador de tarefas            | Ctrl+Shift+Esc ou Executar → `taskmgr`                      |
| `WINVER`                              | Mostra versão do Windows          | Executar → `winver`                                         |

---

## 🧩 Variáveis de Ambiente Úteis

| 🔑 Variável                 | 📝 Descrição                          | 💡 Exemplo / Como usar      |
| --------------------------- | ------------------------------------- | --------------------------- |
| `%HOMEDRIVE%`               | Unidade onde o Windows está instalado | CMD → `echo %HOMEDRIVE%`    |
| `%HOMEPATH%`                | Pasta do usuário atual                | CMD → `echo %HOMEPATH%`     |
| `%PROGRAMFILES%`            | Pasta de instalação de programas      | CMD → `echo %PROGRAMFILES%` |
| `%TEMP%` / `%TMP%`          | Arquivos temporários                  | CMD → `echo %TEMP%`         |
| `%USERPROFILE%`             | Perfil do usuário                     | CMD → `echo %USERPROFILE%`  |
| `%WINDIR%` / `%SYSTEMROOT%` | Pasta do Windows                      | CMD → `echo %WINDIR%`       |

---

## ⚡ Gerenciamento de Processos e Sistema

| ⚡ Comando  | 📝 Descrição                | 💡 Exemplo / Como executar |
| ---------- | --------------------------- | -------------------------- |
| `TASKLIST` | Lista processos em execução | CMD → `tasklist`           |
