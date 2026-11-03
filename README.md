# Free grainy gradients, grain texture PNG + grainy gradient CSS

Live site: https://arnavjhajharia.github.io/grainy-gradients/

| What | Where |
|---|---|
| 6 free grainy mesh-gradient wallpapers (3 desktop 3840×2160, 3 phone 1290×2796) | [`free/`](free/) · [page](https://arnavjhajharia.github.io/grainy-gradients/) |
| Free **seamless transparent grain texture PNG**, white and black, 1024×1024 tile | [`grain-texture/free/`](grain-texture/free/) · [live preview + CSS](https://arnavjhajharia.github.io/grainy-gradients/grain-texture/) |
| Grainy gradient background in pure CSS (SVG `feTurbulence`, no image files) | [page, CSS section](https://arnavjhajharia.github.io/grainy-gradients/#css) |

## Grain overlay in CSS (quick version)

```css
.grainy { position: relative; isolation: isolate; }
.grainy::after {
  content: "";
  position: absolute;
  inset: 0;
  background: url(grain-texture-white-1024.png) 0 0 / 1024px repeat;
  mix-blend-mode: overlay;   /* or soft-light */
  opacity: .35;
  pointer-events: none;
}
```

Keep `background-size` at the PNG's own size (1024px) or half of it on Retina screens. Smaller sizes average the grain away.

## License

The files in `free/` and `grain-texture/free/` may be used in personal and commercial work, including client work, without attribution. Please don't redistribute them as-is as wallpapers, textures or stock; link to the page instead.

## More

- 100 grainy gradient backgrounds + 8 seamless grain overlays: [MESHGRAIN](https://bharatankh.gumroad.com/l/meshgrain)
- The 8 overlays alone (fine, soft, coarse and film grain at 2048 px; paper, dust, halftone and scanlines at 4096 px): [GRAIN + NOISE](https://bharatankh.gumroad.com/l/grain)

Everything here is generated procedurally (numpy, frequency-domain noise on a torus), not by an AI image model.
