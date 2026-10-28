# VectoSolve plugin

Turn raster images into vector files from your AI assistant or editor. This plugin connects the hosted [VectoSolve](https://vectosolve.com) MCP server, `https://vectosolve.com/api/mcp` (Streamable HTTP). No sign-in and no API key.

## What it does

One read-only tool, `vectorize`. Give it a public link to a PNG, JPG, WebP or GIF image (up to 10 MB) and it returns a PNG preview and the complete file:

- **SVG** for design tools, Cricut Design Space and the web
- **DXF** for laser cutters, CNC routers and CAD (R12 polylines, millimetres)
- **EPS** for print and sign-making

Modes: `standard` (logos, illustrations), `laser` (closed cut paths), `cricut` (cutting machines), `centerline` (one path per stroke, for line art and scanned drawings).

## Example prompts

- Vectorize https://vectosolve.com/favicon-512.png
- Turn https://vectosolve.com/favicon-512.png into a DXF for my laser cutter
- Make this drawing a single-line centerline SVG: `<public image link>`

## Contents

- `.cursor-plugin/plugin.json`: plugin manifest
- `mcp.json` / `.mcp.json`: remote MCP server configuration
- `assets/logo.png`: icon

## Manual setup

Any client that supports remote MCP servers can use the endpoint directly:

```json
{
  "mcpServers": {
    "vectosolve": { "url": "https://vectosolve.com/api/mcp" }
  }
}
```

## Links

- Documentation: https://vectosolve.com/integrations/mcp
- Official MCP Registry: `io.github.Vectosolve/vectosolve`
- Privacy: https://vectosolve.com/privacy
- Terms: https://vectosolve.com/terms
- Support: contact@vectosolve.com

## License

MIT for the contents of this repository. The hosted VectoSolve service is subject to its [terms](https://vectosolve.com/terms).
