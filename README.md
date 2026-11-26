# Futsal Live! Android — Distribuição

Este repositório público disponibiliza **exclusivamente as versões instaláveis** do Futsal Live! Android e o manifesto de atualizações. O código-fonte, os dados dos jogos, os jogadores e as chaves de assinatura **não são publicados aqui**.

## Estado

A infraestrutura de atualização está implementada no projeto privado `MarcosMig/Futsal-Performance-Hub` (branch `feature/android-live-autonomous-foundation`), mas **ainda não há APK estável publicada neste repositório**. Não instalar versões para utilização oficial em jogos.

## Convenção de publicação

1. Compilar uma APK release com a **mesma chave de assinatura permanente** e um `versionCode` superior ao anterior.
2. Criar uma GitHub Release com a tag `vX.Y.Z` e anexar a APK com nome `futsal-live.apk`.
3. Calcular SHA-256 da APK publicada e criar/atualizar `live-update.json` na branch `main`:

```json
{
  "application_id": "pt.fperformance.live",
  "version_code": 4,
  "version_name": "0.1.3-alpha",
  "apk_url": "https://github.com/MarcosMig/Futsal-Live-Android-Releases/releases/download/v0.1.3-alpha/futsal-live.apk",
  "sha256": "SUBSTITUIR_PELO_SHA256_REAL_DE_64_CARACTERES"
}
```

O exemplo acima **não é um manifesto operativo**; publicar `live-update.json` apenas quando a APK real existir. A app irá obter o manifesto via `https://raw.githubusercontent.com/MarcosMig/Futsal-Live-Android-Releases/main/live-update.json`.

## Segurança

- Nunca adicionar keystores (`.jks`, `.keystore`), passwords, tokens, bases de dados ou relatórios.
- As atualizações exigem confirmação do utilizador pelo instalador Android.
- O sistema Android valida o certificado de assinatura da atualização. Uma APK debug assinada por outra chave **não atualiza** uma instalação existente.
- Antes da primeira instalação estável, fazer uma cópia de segurança dos dados importantes da versão de testes.
