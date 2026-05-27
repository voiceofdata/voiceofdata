---

---

# Sales and Support Productivity

<div class="project-tools case-study-tools" aria-label="Tools used">
  <span class="expertise-tag project-tool-pill">Power BI</span>
  <span class="expertise-tag project-tool-pill">DAX</span>
  <span class="expertise-tag project-tool-pill">Power Query</span>
  <span class="expertise-tag project-tool-pill">Figma</span>
</div>

This report was built over four years at a software reseller, growing from a single landing page into a 13-page, 244-measure dashboard used by AE managers, COS team leads, and eventually the Finance VP. It wasn't scoped that way from the start — it expanded because people found it useful and kept asking for more.

The analytical thread running through every page is the COS support model: a structure where Client Operations Specialists create and manage transactions on behalf of Account Executives, with support assignments tracked at the client level. Every standard company report was AE-coded — the COS team had no visibility into their own activity or performance. This report was built to fix that. The AE pages exist too, but as a secondary lens; the primary question the report was designed to answer is how the COS team is performing, who they're supporting, and whether that support is translating into qualified revenue.

The technical problems worth talking about are the ones Power BI doesn't solve natively. Qualification status across Hardware and Software lines required a six-state conditional formatting system — Qualified, Nearly Qualified, and Not Qualified, each with and without COS support assigned — encoded as custom icons built in Figma and imported via theme JSON. A MoM/YoY view toggle on the AE detail page predates field parameters and was implemented with bookmarks and styled buttons. Percentage measures on the Account Executives page calculate denominators dynamically based on matrix expansion level, shifting context between the overall team, an individual AE, and their support breakdown without separate measures for each level. Across the report, measure-driven text strings surface contextual information inline — supported AE counts, assigned COS names, qualification summaries — rather than relying on card visuals or static labels.

The report was built to be used by people who didn't build it, and that shaped some decisions that don't show up in screenshots. An About page documents the acronyms, team structures, and page purposes for anyone coming in cold. A hidden dev notes page captures implementation details and design decisions — internal documentation that made handing the report off or returning to it after months away significantly less painful. The original file also included an embedded data dictionary built using Power BI's INFO functions, surfacing table and column metadata directly inside the report without needing an external document.

Scope expanded through real stakeholder demand. The Finance VP requested executive summary pages — one for the AE organisation, one for the COS team — giving leadership a single-screen view without needing to navigate the detail pages. A team manager requested the AE Product Mix page to track line of business split at the rep level. Neither was in the original brief. The report stayed coherent despite the additions because the COS support thread runs through every page, including the ones that weren't originally planned.

For the portfolio version, the report was rebuilt from scratch using synthetic data generated via a custom Python script to eliminate anything sensitive. The rebuild used Power BI's PBIP format rather than PBIX, which allows the underlying TMDL files to be edited directly in a text editor. All 244 measures were migrated via find-and-replace on the TMDL files rather than rebuilt through the UI — an approach that's only possible if you understand what's actually inside the file format, and one that reduced what could have been weeks of rework to a single pass.


## Screenshots

### Executive AE
*Leadership summary page showing revenue, GP, and quote/order volume with COS support breakdown across all metrics.*
![Executive AE](Productivity%20-%20Exec%20AE.png)

### Executive ClientOps
*Mirror page from the COS team lens, pre-filtered to a single team.*
![Executive ClientOps](Productivity%20-%20Exec%20COS.png)

### Client Ops Summary
*At-a-glance team comparison with COS count and full metric breakdown per team. No team filter — the columns are structural.*
![Client Ops Summary](Productivity%20-%20COS%20Summary.png)

### ClientOps Team Summary
*Team-level detail with field parameter-driven column selection and bookmark-based table toggle.*
![ClientOps Team Summary](Productivity%20-%20COS%20Team%20Summary.png)

### ClientOps Team Detail
*Full metric matrix with conditional formatting arrows and QoQ/YoY comparisons per COS/AE pairing.*
![ClientOps Team Detail](Productivity%20-%20COS%20Team%20Detail.png)

### AE Team Summary
*AE-side equivalent of the Client Ops Summary, with COS support percentage visible on every volume metric.*
![AE Team Summary](Productivity%20-%20AE%20Team%20Summary.png)

### Account Executives
*Expandable matrix with context-sensitive percentage denominators shifting by hierarchy level.*
![Account Executives](Productivity%20-%20AE.png)

### AE Team Detail — YoY
![AE Team Detail YoY](Productivity%20-%20AE%20Team%20Detail%20YoY.png)

### AE Team Detail — MoM
*MoM/YoY toggle implemented via bookmarks and styled buttons — no native toggle exists in Power BI.*
![AE Team Detail MoM](Productivity%20-%20AE%20Team%20Detail%20MoM.png)

### AE Sales Qualification Summary
*DAX-driven qualification classification across Hardware and Software thresholds, with dynamic support assignment indicators.*
![AE Sales Qualification Summary](Productivity%20-%20AE%20Support%20Qualify%20Summary.png)

### AE Sales 12 Month Rolling — Full View
![AE Sales 12 Month Rolling Full](Productivity%20-%20AE%20Support%20Qualify%20Details.png)

### AE Sales 12 Month Rolling — Single AE
*Six-state custom icons built in Figma and imported via theme JSON, encoding qualification level and COS assignment status in a single visual element.*
![AE Sales 12 Month Rolling Single AE](Productivity%20-%20AE%20Support%20Qualify%20Details%20%281%20person%29.png)
