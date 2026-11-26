# Futsal Live! Android — APK e atualizações

Este repositório público contém **apenas APK assinadas e o manifesto de atualizações**. O código-fonte, as bases de dados dos jogos e a chave de assinatura permanecem privados.

## Versão disponível

**0.1.7-alpha (versão de testes, assinatura permanente)**

- [Descarregar APK para Android](https://github.com/MarcosMig/Futsal-Live-Android-Releases/raw/refs/heads/main/apk/futsal-live-0.1.7-alpha.apk)
- [Consultar manifesto de atualizações](https://raw.githubusercontent.com/MarcosMig/Futsal-Live-Android-Releases/main/live-update.json)
- SHA-256 da APK: `f0731eacc516a9788e06a1106d96829b83a551f525fc72f7e4890dd1228a18d3`

### Instalação

- A instalação fora da Play Store exige que o utilizador permita esta origem de instalação e confirme a operação no Android.
- **Esta APK é uma versão técnica de ensaio, não adequada a ser usada como único cronómetro em jogo oficial.**
- Se uma versão debug anterior (`0.1.1` ou `0.1.2-alpha`) estiver instalada com outra assinatura, o Android poderá recusar esta instalação. **Desinstalar a aplicação antiga apaga os dados locais**; não o faças antes de guardar quaisquer jogos ou estatísticas importantes.
- Depois da primeira instalação **assinada permanentemente**, versões futuras com o mesmo identificador e a mesma assinatura poderão atualizar sem eliminar os dados locais.

### Como funcionam as atualizações seguintes

O botão **Verificar atualização** da aplicação consulta `live-update.json`, compara `version_code`, confirma o SHA-256 da APK e abre o instalador oficial Android. A Internet é necessária para verificar e descarregar; o registo de jogo funciona em rede local sem Internet.

As novas versões devem aumentar o `version_code` e publicar um novo ficheiro APK assinado com **a mesma chave privada**, seguido da atualização do manifesto. Nunca publicar chaves, passwords, tokens ou bases de dados neste repositório.

## Teste de atualização 0.1.3 → 0.1.4

Se já instalaste **0.1.3-alpha assinada permanentemente**, não descarregues a 0.1.4 manualmente: abre a app, toca em **Verificar atualização**, confirma o download e segue o instalador Android. O Android deve preservar os dados locais porque as duas APK usam a mesma chave. Confirma depois os jogadores e o jogo de teste.

## Correção 0.1.5

Após uma atualização ou reinício do servidor Android, os antigos logins temporários deixam de existir; por isso as funções exclusivas são libertadas ao arrancar. Os jogos, atletas e eventos mantêm-se. Também existe um comando **Recuperar função** mediante código de emparelhamento para operadores que fiquem bloqueados durante a sessão. Não o utilizar se o operador anterior ainda estiver ativo.

## Sincronizar o plantel (teste 0.1.7)

No tablet principal, o botão **Sincronizar plantel** solicita as credenciais da conta Performance Hub e descarrega os atletas pela API autenticada. Os nomes, posições, números e fotografias são armazenados localmente, para consulta offline. Apenas o email é lembrado no tablet; não se guardam passwords nem tokens. Os outros tablets recebem os cartões através da rede local.

**Esta funcionalidade ainda precisa de validação em dispositivo físico com uma conta Hub ativa.** A aplicação continua a ser um protótipo de testes, não deve ser utilizada como único cronómetro oficial.
