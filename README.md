# FNF Update Checker System 🎮

Um sistema de verificação de atualização automático para mods de Friday Night Funkin'.

## Como usar no seu mod

### 1. Copie os dois arquivos para a pasta `scripts/` do seu mod:
- `scripts/UpdateChecker.hxc` — lógica principal (não edite!)
- `UpdateCheckerConfig.hxc` — suas configurações (edite aqui!)

### 2. Crie um `UpdateCheckerConfig.hxc` na pasta `scripts/` do seu mod:

```haxe
import funkin.modding.module.Module;

class UpdateCheckerConfig extends Module {
    public var modID:String = "SEU_MOD_ID_AQUI";      // ID do GameBanana
    public var versaoAtual:String = "1.0.0";           // Versão atual do mod
    public var modFolderName:String = "SuaPastaDoMod"; // Nome da pasta em mods/
    function new() { super("UpdateCheckerConfig"); }
}
```

### 3. Coloque as imagens na pasta `images/` do seu mod:
- `images/updateBG.png` — fundo do popup (900x680)
- `images/updateScrim.png` — gradiente na thumbnail (qualquer tamanho)

> A pasta `images/` desse repositório contém as imagens originais do SYNK mod.

---

## Como atualizar o sistema para TODOS os seus usuários

1. Modifique `scripts/UpdateChecker.hxc` nesse repositório
2. Incremente a versão em `CORE_VERSION` dentro do arquivo
3. Atualize `version.txt` com a mesma versão
4. Faça commit e push

Na próxima vez que os usuários abrirem o jogo com internet, o sistema se atualiza automaticamente em background. O efeito é aplicado no próximo boot do jogo.

---

## Versão atual do sistema
Ver `version.txt`
