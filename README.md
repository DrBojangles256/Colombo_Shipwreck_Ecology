COLOMBO / WRECKS & REEFS — STORYMAPS EMBED PACKAGE

Files
index.html: responsive standalone interactive dashboard; no build step or API key.
colombo-sites.geojson / .csv: six study locations transcribed from Table 1.

Deploy
1. Extract the ZIP. Upload index.html to an HTTPS static website (your organization web server, GitHub Pages, or another approved static host). Keep the filename index.html.
2. Visit the public HTTPS page and check basemap tiles, all six markers, site selection, filters, search, and GeoJSON export.
3. In ArcGIS StoryMaps add an Embed block, paste the hosted page URL, and select a live embed. Use a large block or sidecar media panel. Suggested available height: 800–900 px.
4. Preview desktop and mobile and test the published story, not only the builder.

A local HTML file cannot be pasted into StoryMaps as application source code. Hosting is required. StoryMaps accepts a URL or iframe, not pasted script code.
Optional iframe template (replace the placeholder with your actual deployed URL):
<iframe src="YOUR_HOSTED_HTTPS_URL" title="Colombo shipwreck and natural reef dashboard" width="100%" height="850" style="border:0" loading="lazy"></iframe>

Security / dependencies
Do not send X-Frame-Options: DENY or SAMEORIGIN. Ensure any Content-Security-Policy frame-ancestors permits https://storymaps.arcgis.com and your actual Enterprise StoryMaps origin if used. Coordinate with your administrator; do not disable unrelated security protections.
Leaflet 1.9.4 JS/CSS loads from unpkg.com. Satellite tiles load from server.arcgisonline.com; dark tiles from basemaps.cartocdn.com. These require internet access and host/network permission. For strict production security, self-host vetted Leaflet files and apply your organization's CSP and dependency policies. Review third-party basemap service terms for your deployment.
The app has no login, server, analytics or editing endpoints. Scroll-wheel zoom is disabled to reduce scroll capture inside a story; map zoom buttons and touch gestures remain available.

Evidence
Hannak A, Puebla O, Perera N (2025). Fish assemblages on shipwrecks versus natural reefs in Colombo, Sri Lanka. Bulletin of Marine Science 101(1):179–195. DOI: 10.5343/bms.2023.0109.
Coordinates, depths, ship dimensions and dates use Table 1, p. 182. Descriptive habitat text uses Methods, pp. 181–184. Coordinate conversion: decimal degrees = degrees + decimal minutes / 60. Coordinate reference system is not explicitly stated in Table 1; positions are interpreted as geographic longitude/latitude for web display. Precision of decimal output is not a positional accuracy claim.
Natural reefs are points, not invented polygons. The mining screenshot is a visual palette reference only. No mining data are included.
Mean densities and SE are published habitat-level values. No per-site fish density or species counts were inferred. Raw totals reflect unequal sampling effort. No density significance claim is made. Table 1 values are preferred over conflicting narrative dimensions; discrepancies are disclosed inside the dashboard.

Validation status
Source coordinates and records were checked computationally; this environment does not provide a browser or public hosting. Live rendering, tile service availability and embedding must be tested on the deployment host.
