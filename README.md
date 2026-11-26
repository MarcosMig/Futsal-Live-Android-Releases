# Futsal Live! Android — APK e atualizações

Este repositório público contém **apenas APK assinadas e o manifesto de atualizações**. O código-fonte, as bases de dados dos jogos e a chave de assinatura permanecem privados.

## Versão disponível

**0.1.3-alpha (versão de testes, assinatura permanente)**

- [Descarregar APK para Android](https://github.com/MarcosMig/Futsal-Live-Android-Releases/raw/refs/heads/main/apk/futsal-live-0.1.3-alpha.apk)
- [Consultar manifesto de atualizações](https://raw.githubusercontent.com/MarcosMig/Futsal-Live-Android-Releases/main/live-update.json)
- SHA-256 da APK: `ce6c502d363ce9a9fbcc91770429e718cc8a2bb4f907db757d21b8571c174ede`

### Instalação

- A instalação fora da Play Store exige que o utilizador permita esta origem de instalação e confirme a operação no Android.
- **Esta APK é uma versão técnica de ensaio, não adequada a ser usada como único cronómetro em jogo oficial.**
- Se uma versão debug anterior (`0.1.1` ou `0.1.2-alpha`) estiver instalada com outra assinatura, o Android poderá recusar esta instalação. **Desinstalar a aplicação antiga apaga os dados locais**; não o faças antes de guardar quaisquer jogos ou estatísticas importantes.
- Depois da primeira instalação **assinada permanentemente**, versões futuras com o mesmo identificador e a mesma assinatura poderão atualizar sem eliminar os dados locais.

### Como funcionam as atualizações seguintes

O botão **Verificar atualização** da aplicação consulta `live-update.json`, compara `version_code`, confirma o SHA-256 da APK e abre o instalador oficial Android. A Internet é necessária para verificar e descarregar; o registo de jogo funciona em rede local sem Internet.

As novas versões devem aumentar o `version_code` e publicar um novo ficheiro APK assinado com **a mesma chave privada**, seguido da atualização do manifesto. Nunca publicar chaves, passwords, tokens ou bases de dados neste repositório.
