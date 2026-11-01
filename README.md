# Funilar Gestão

Gestão da oficina: carros e O.S. (recepção com checklist, tarefas, insumos liberados por funcionário, custo real), estoque com endereço e fotos, equipe (pintor, funileiro, martelinho…), financeiro com vendas, caixa e resultado por funcionário.

Faz parte da família **Funilar**: o Funilar completo (repositório `robervall-app`) junta tudo;
este sistema traz só a sua parte e funciona sozinho, com os próprios dados.
Android, iPhone, Windows e Linux (Flutter). Funciona offline; os dados ficam no aparelho.

## Baixar
Cada push na `main` compila no GitHub Actions e publica em **Releases**:
`Gestao-android.apk`, `Gestao-windows-x64.zip`, `Gestao-linux-x64.tar.gz`
(iPhone: `[ios]` na mensagem do commit gera `Gestao-ios-sem-assinatura.ipa`).

No Windows, para instalar ou atualizar pelo PowerShell:
```powershell
irm https://raw.githubusercontent.com/Pedroedmachado/gestao-oficina/main/tool/atualizar-gestao_oficina.ps1 | iex
```
Dentro do app: **Ajustes › Atualizações**.

## Backup entre os sistemas
O backup (.zip) de qualquer sistema Funilar pode ser restaurado em outro —
por exemplo, levar os cadastros para o Funilar completo.

## Compilar na sua máquina
```bash
bash tool/prepare_platforms.sh   # gera android/, ios/, linux/, windows/
flutter pub get
flutter test
flutter run
```

## Código
Este repositório é gerado a partir do Funilar completo
(`bash tool/gerar_modulos.sh gestao <pasta>` no `robervall-app`), por isso as correções
feitas lá chegam aqui na próxima geração.
