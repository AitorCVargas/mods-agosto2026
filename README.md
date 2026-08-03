# MC Comunidad Optimized (packwiz)

Pack NeoForge **1.21.1** / **21.1.248** con configs potato, resource packs y shaders (OFF).

## Jugadores (auto-update)

1. Instala **Prism Launcher** (recomendado para updates automáticos).
2. Importa el zip `MC_Comunidad_Prism.zip` (te lo pasa Aitor).
3. Cada vez que abras la instancia, **packwiz** mira este repo y descarga mods/configs nuevos.

URL del pack:

```text
https://raw.githubusercontent.com/AitorCVargas/mods-agosto2026/main/pack.toml
```

RAM: 4–6 GB. Shaders: Video → Shader Packs (vienen desactivados).

> El repo debe ser **público** para que el instalador pueda leer `pack.toml` sin token.

## Aitor — cómo actualizar (para todos)

1. Prueba los cambios en tu perfil Modrinth (`MC_1.21.1_Optimized_Test`).
2. Regenera el packwiz desde el perfil:

```powershell
cd C:\Users\Aitor\Downloads\MODS
python build_comunidad_pack.py
```

3. Copia lo nuevo a este repo (o trabaja directo aquí) y sube:

```powershell
cd C:\Users\Aitor\Downloads\MODS\comunidad_pack
git add -A
git commit -m "update: descripcion corta"
git push
```

4. La gente **no hace nada**: al abrir Minecraft, Prism corre packwiz y sincroniza.

### Añadir un solo mod a mano

```powershell
cd C:\Users\Aitor\Downloads\MODS\comunidad_pack
.\packwiz.exe mr add slug-del-mod -y
.\packwiz.exe refresh -y
git add -A
git commit -m "add: nombre-del-mod"
git push
```

### Actualizar mods del índice

```powershell
.\packwiz.exe update --all -y
.\packwiz.exe refresh -y
git add -A
git commit -m "chore: update mods"
git push
```
