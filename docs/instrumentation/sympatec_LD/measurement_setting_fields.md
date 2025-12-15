# Product Parameters — What to Fill Out (Lab Standard)

The **Product Parameters** tab defines the *material identity and physical assumptions* used to interpret the measurement.  
These fields should be **stable**, **intentional**, and **reused via templates** whenever possible.

Do **not** use this tab to encode run-level details (replicates, dates, flow rate, operator).

---

## Product Name
**What to enter:**  
- The **API identity only**
- Include the **full salt form**, if applicable

**Examples:**
- `Niclosamide`
- `Colistin sulfate`
- `Lysozyme`
- `Mannitol` or `PVP` if working with an API-free control
- If a mixture of two APIs is used, include both in the product name (e.g., `niclosamide_colistin-sulfate`) 

**Do NOT include:**
- excipients (e.g., PVP, leucine, mannitol) - The exception to this is if no API is present. In this case, use the excipient with the highest % as the product name
- processing method
- formulation ratios
- DOE identifiers
- replicate numbers
- dates or pressures

> Rule of thumb:  
> If the **API or salt form changes**, the Product name should change.  
> Changes in excipients, ratios, or processing should *not* change the Product name.

---

## Density
**What to enter:**  
- The best available estimate of **true particle density** (g/cm³)

**Guidance:**
- Use literature or experimentally justified values when available
- If unknown, use a documented placeholder (1 g/cm³) and update later if needed

**Important:**  
This value affects calculated surface-area-based metrics.

---

## Heywood Shape Factor
**What to enter:**  
- Default = `1.0` unless there is a strong, justified reason to change it

**Guidance:**
- Treat this as a **physics assumption**, not a tuning parameter
- Changes should be rare and deliberate

---

## Quality Limits
**What to do:**  
- Leave unchecked unless explicitly instructed otherwise

**Note:**  
Quality limits are optional validation constraints and are not required for routine measurements.

---

## Additional Parameters (Structured Metadata)
Use **Additional Parameters** to capture stable descriptors that should *not* live in the Product name.

### Required / Recommended Fields

#### `process`
**Type:** Text  
**What to enter:** One of the following (use consistent spelling):
- `spray_dried`
- `milled`
- `LAP`
- `unprocessed`
- `SFD`
- `lyophilized`

---

#### `formulation_id`
**Type:** Text  
**What to enter:**  
- **Full formulation composition and ratios**, including excipients

**Examples:**
- `COL-NIC_8-1`
- `NIC-PVP-LEU_10-80-10`

**Rules:**
- Components separated by `-`
- Ratios separated by `_`
- Order of ratios matches order of components
- Excipients belong **here**, not in the Product name

> Note:  
> `formulation_id` encodes *what is in the formulation and in what ratios*.  
> It should change when excipients or ratios change.

---

#### `DOE_id` (only if applicable)
**Type:** Text  
**What to enter:** Identifier for a formal design-of-experiments study

**Examples:**
- `DOE-2024-01`
- `LAP_DOE_A`
- `MixtureDOE_v2`

Leave blank if the run is not part of a DOE.

---

## Product-Specific Comment
**What to use this for:**  
- Narrative notes
- Special preparation details
- Context not captured elsewhere

**Do NOT rely on this field for structured data.**

---

## Summary Rule Set
- **Product name** = API identity (including salt form only)  
- **Additional Parameters** = formulation composition (including excipients), ratios, and processing  
- **User Parameters** = who ran it and which specific instance was measured  

Keeping this separation clean ensures reproducible data, reusable templates, and analyzable exports.
