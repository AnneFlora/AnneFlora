import { useState } from "react";

Hi, I'm Anne Flora 👋

Associate Analyst at Accenture, transitioning into Business Analysis.
I spend my days turning messy operational data into clear decisions — through dashboards, process maps, and structured documentation.

I'm not starting from zero. I've spent 1.6 years in incident management and process improvement, reducing resolution times, automating reports, and building KPI dashboards that people actually use. Now I'm formalising that into a BA career.

---

## 🧩 What I Do

| Area | What it looks like in practice |
|---|---|
| **Process Analysis** | Mapping ticket workflows, identifying bottlenecks, proposing fixes |
| **Data Reporting** | Excel dashboards with slicers, KPI tracking, pivot tables |
| **Requirements Gathering** | Translating stakeholder needs into structured documentation |
| **Automation** | Excel macros that saved 5+ hours/week in manual effort |
| **Root Cause Analysis** | Diagnosing recurring failures before they repeat |

---

## 🔧 Tools & Tech

**Currently using:**
Excel (Advanced) · PowerPoint · Mainframe/ITSM · MS Office Suite

**Actively building:**
SQL · Power BI · Process Mapping (Draw.io) · Agile/JIRA

---

## 📁 Projects

### 📊 Incident Trend Analysis Dashboard
*Excel · Pivot Tables · Slicers · 2025*

Cleaned 6 months of raw incident log data, built an interactive Excel dashboard with KPI metrics and slicers so stakeholders could self-serve insights — no analyst needed for every query. One recommendation from this dashboard led to a ~40% reduction in a recurring error category.

---

### 🗺️ Ticket Resolution Process Map
*Excel · PowerPoint · 2024*

Mapped the full end-to-end ticket resolution workflow, surfaced 4 key bottlenecks, and presented a structured business case to supervisors with a revised workflow proposal.

---

## 🚧 Currently Building

- **SQL fundamentals** — working through structured query practice daily
- **Power BI basics** — moving dashboards beyond Excel
- **BA documentation skills** — BRDs, user stories, process maps
- **90-day BA transition plan** — building a portfolio to match the career pivot

---

## 🎓 Background

**B.E. Computer Science & Engineering** — Panimalar Engineering College (2020–2024)
Relevant: DBMS, Data Structures, Statistics, Software Engineering

**Certifications in progress:**
- Google Data Analytics Professional Certificate (Coursera)
- Microsoft Excel for Business & Data Analysis (Coursera)
- Business Analysis Foundations (Coursera)
- SQL for Data Analysis (Mode Analytics)

---

## 📬 Reach Me

- 📧 anneflora2003@gmail.com
- 💼 [linkedin.com/in/anneflora](https://linkedin.com/in/anneflora)
- 📍 Thiruvallur, Tamil Nadu

---

*Open to entry-level BA or DA roles. If you're hiring for someone who can bridge operations and analysis — let's talk.*`;

export default function GitHubProfile() {
  const [tab, setTab] = useState("preview");
  const [copied, setCopied] = useState(null);

  const copyText = (text, key) => {
    navigator.clipboard.writeText(text).then(() => {
      setCopied(key);
      setTimeout(() => setCopied(null), 2000);
    });
  };

  const sections = [
    { id: "intro", label: "Intro" },
    { id: "what", label: "What I Do" },
    { id: "tools", label: "Tools" },
    { id: "projects", label: "Projects" },
    { id: "building", label: "Building" },
    { id: "contact", label: "Contact" },
  ];

  return (
    <div style={{
      fontFamily: "'Georgia', 'Times New Roman', serif",
      background: "#0d1117",
      minHeight: "100vh",
      color: "#e6edf3",
      padding: "0",
    }}>
      {/* Header */}
      <div style={{
        background: "linear-gradient(135deg, #161b22 0%, #0d1117 60%)",
        borderBottom: "1px solid #21262d",
        padding: "32px 40px 24px",
      }}>
        <div style={{ maxWidth: 860, margin: "0 auto" }}>
          <div style={{ display: "flex", alignItems: "center", gap: 16, marginBottom: 8 }}>
            <div style={{
              width: 48, height: 48, borderRadius: "50%",
              background: "linear-gradient(135deg, #238636, #1f6feb)",
              display: "flex", alignItems: "center", justifyContent: "center",
              fontSize: 20, fontWeight: 700, fontFamily: "monospace",
              color: "#fff", flexShrink: 0,
            }}>AF</div>
            <div>
              <div style={{ fontSize: 22, fontWeight: 700, fontFamily: "'Georgia', serif", color: "#f0f6fc" }}>
                Anne Flora R
              </div>
              <div style={{ fontSize: 13, color: "#8b949e", fontFamily: "monospace" }}>
                AnneFlora · GitHub Profile README
              </div>
            </div>
          </div>
        </div>
      </div>

      {/* Tab Bar */}
      <div style={{
        background: "#161b22",
        borderBottom: "1px solid #21262d",
        padding: "0 40px",
      }}>
        <div style={{ maxWidth: 860, margin: "0 auto", display: "flex", gap: 0 }}>
          {["preview", "raw"].map(t => (
            <button
              key={t}
              onClick={() => setTab(t)}
              style={{
                background: "none", border: "none",
                borderBottom: tab === t ? "2px solid #f78166" : "2px solid transparent",
                color: tab === t ? "#f0f6fc" : "#8b949e",
                padding: "12px 20px",
                fontSize: 14, cursor: "pointer",
                fontFamily: "monospace",
                textTransform: "uppercase",
                letterSpacing: "0.05em",
                transition: "color 0.2s",
              }}
            >{t}</button>
          ))}
        </div>
      </div>

      <div style={{ maxWidth: 860, margin: "0 auto", padding: "32px 40px" }}>

        {tab === "preview" && (
          <div>
            {/* Bio Section */}
            <div style={{
              background: "#161b22",
              border: "1px solid #21262d",
              borderRadius: 10,
              padding: "24px 28px",
              marginBottom: 24,
            }}>
              <div style={{
                display: "flex", justifyContent: "space-between",
                alignItems: "flex-start", marginBottom: 16,
              }}>
                <div>
                  <span style={{
                    fontSize: 11, fontFamily: "monospace",
                    color: "#f78166", textTransform: "uppercase",
                    letterSpacing: "0.1em", fontWeight: 700,
                  }}>GitHub Bio</span>
                  <span style={{
                    marginLeft: 12, fontSize: 11,
                    color: "#8b949e", fontFamily: "monospace",
                  }}>{bioText.length} / 150 chars</span>
                </div>
                <button
                  onClick={() => copyText(bioText, "bio")}
                  style={{
                    background: copied === "bio" ? "#238636" : "#21262d",
                    border: "1px solid #30363d",
                    borderRadius: 6, color: "#f0f6fc",
                    padding: "6px 14px", fontSize: 12,
                    fontFamily: "monospace", cursor: "pointer",
                    transition: "background 0.2s",
                  }}
                >{copied === "bio" ? "✓ Copied" : "Copy"}</button>
              </div>
              <div style={{
                fontSize: 15, color: "#e6edf3",
                lineHeight: 1.6, fontFamily: "'Georgia', serif",
                borderLeft: "3px solid #1f6feb",
                paddingLeft: 16,
              }}>
                {bioText}
              </div>
            </div>

            {/* README Preview */}
            <div style={{
              background: "#161b22",
              border: "1px solid #21262d",
              borderRadius: 10,
              overflow: "hidden",
            }}>
              <div style={{
                padding: "14px 24px",
                borderBottom: "1px solid #21262d",
                display: "flex", justifyContent: "space-between",
                alignItems: "center",
              }}>
                <span style={{ fontSize: 12, fontFamily: "monospace", color: "#8b949e" }}>
                  📄 README.md
                </span>
                <button
                  onClick={() => copyText(readmeRaw, "readme")}
                  style={{
                    background: copied === "readme" ? "#238636" : "#21262d",
                    border: "1px solid #30363d",
                    borderRadius: 6, color: "#f0f6fc",
                    padding: "6px 14px", fontSize: 12,
                    fontFamily: "monospace", cursor: "pointer",
                    transition: "background 0.2s",
                  }}
                >{copied === "readme" ? "✓ Copied" : "Copy README"}</button>
              </div>

              <div style={{ padding: "32px 36px" }}>
                {/* Intro */}
                <h1 style={{ fontSize: 26, fontWeight: 700, color: "#f0f6fc", marginBottom: 12, fontFamily: "'Georgia', serif" }}>
                  Hi, I'm Anne Flora 👋
                </h1>
                <p style={{ color: "#8b949e", fontSize: 14, fontFamily: "monospace", marginBottom: 6 }}>
                  Associate Analyst at Accenture, transitioning into Business Analysis.
                </p>
                <p style={{ color: "#c9d1d9", lineHeight: 1.7, marginBottom: 8 }}>
                  I spend my days turning messy operational data into clear decisions — through dashboards, process maps, and structured documentation.
                </p>
                <p style={{ color: "#c9d1d9", lineHeight: 1.7, marginBottom: 28 }}>
                  I'm not starting from zero. I've spent 1.6 years in incident management and process improvement, reducing resolution times, automating reports, and building KPI dashboards that people actually use. Now I'm formalising that into a BA career.
                </p>

                <hr style={{ border: "none", borderTop: "1px solid #21262d", marginBottom: 28 }} />

                {/* What I Do */}
                <h2 style={{ fontSize: 18, fontWeight: 700, color: "#f0f6fc", marginBottom: 14 }}>🧩 What I Do</h2>
                <table style={{ width: "100%", borderCollapse: "collapse", marginBottom: 28, fontSize: 14 }}>
                  <thead>
                    <tr style={{ background: "#0d1117" }}>
                      <th style={{ textAlign: "left", padding: "10px 14px", color: "#8b949e", fontWeight: 600, borderBottom: "1px solid #21262d", width: "35%" }}>Area</th>
                      <th style={{ textAlign: "left", padding: "10px 14px", color: "#8b949e", fontWeight: 600, borderBottom: "1px solid #21262d" }}>In practice</th>
                    </tr>
                  </thead>
                  <tbody>
                    {[
                      ["Process Analysis", "Mapping ticket workflows, identifying bottlenecks, proposing fixes"],
                      ["Data Reporting", "Excel dashboards with slicers, KPI tracking, pivot tables"],
                      ["Requirements Gathering", "Translating stakeholder needs into structured documentation"],
                      ["Automation", "Excel macros that saved 5+ hours/week in manual effort"],
                      ["Root Cause Analysis", "Diagnosing recurring failures before they repeat"],
                    ].map(([area, desc], i) => (
                      <tr key={i} style={{ background: i % 2 === 0 ? "#161b22" : "#0d1117" }}>
                        <td style={{ padding: "10px 14px", color: "#79c0ff", fontWeight: 600, borderBottom: "1px solid #21262d" }}>{area}</td>
                        <td style={{ padding: "10px 14px", color: "#c9d1d9", borderBottom: "1px solid #21262d" }}>{desc}</td>
                      </tr>
                    ))}
                  </tbody>
                </table>

                <hr style={{ border: "none", borderTop: "1px solid #21262d", marginBottom: 28 }} />

                {/* Tools */}
                <h2 style={{ fontSize: 18, fontWeight: 700, color: "#f0f6fc", marginBottom: 14 }}>🔧 Tools & Tech</h2>
                <div style={{ display: "flex", gap: 24, marginBottom: 28, flexWrap: "wrap" }}>
                  <div style={{ flex: 1, minWidth: 200 }}>
                    <div style={{ fontSize: 12, color: "#8b949e", fontFamily: "monospace", marginBottom: 8, textTransform: "uppercase", letterSpacing: "0.05em" }}>Currently using</div>
                    {["Excel (Advanced)", "PowerPoint", "Mainframe / ITSM", "MS Office Suite"].map(t => (
                      <div key={t} style={{ display: "inline-block", background: "#21262d", border: "1px solid #30363d", borderRadius: 20, padding: "4px 12px", fontSize: 12, color: "#c9d1d9", margin: "3px 4px 3px 0", fontFamily: "monospace" }}>{t}</div>
                    ))}
                  </div>
                  <div style={{ flex: 1, minWidth: 200 }}>
                    <div style={{ fontSize: 12, color: "#8b949e", fontFamily: "monospace", marginBottom: 8, textTransform: "uppercase", letterSpacing: "0.05em" }}>Actively building</div>
                    {["SQL", "Power BI", "Draw.io", "Agile / JIRA"].map(t => (
                      <div key={t} style={{ display: "inline-block", background: "#0d2818", border: "1px solid #238636", borderRadius: 20, padding: "4px 12px", fontSize: 12, color: "#3fb950", margin: "3px 4px 3px 0", fontFamily: "monospace" }}>{t}</div>
                    ))}
                  </div>
                </div>

                <hr style={{ border: "none", borderTop: "1px solid #21262d", marginBottom: 28 }} />

                {/* Projects */}
                <h2 style={{ fontSize: 18, fontWeight: 700, color: "#f0f6fc", marginBottom: 16 }}>📁 Projects</h2>
                {[
                  {
                    title: "📊 Incident Trend Analysis Dashboard",
                    meta: "Excel · Pivot Tables · Slicers · 2025",
                    desc: "Cleaned 6 months of raw incident log data and built an interactive Excel dashboard with KPI metrics and slicers so stakeholders could self-serve insights — no analyst needed for every query. One recommendation from this dashboard led to a ~40% reduction in a recurring error category.",
                  },
                  {
                    title: "🗺️ Ticket Resolution Process Map",
                    meta: "Excel · PowerPoint · 2024",
                    desc: "Mapped the full end-to-end ticket resolution workflow, surfaced 4 key bottlenecks, and presented a structured business case to supervisors with a revised workflow proposal.",
                  },
                ].map((p, i) => (
                  <div key={i} style={{
                    background: "#0d1117", border: "1px solid #21262d",
                    borderRadius: 8, padding: "20px 22px", marginBottom: 16,
                    borderLeft: "3px solid #1f6feb",
                  }}>
                    <div style={{ fontWeight: 700, color: "#f0f6fc", marginBottom: 4, fontSize: 15 }}>{p.title}</div>
                    <div style={{ fontSize: 11, color: "#8b949e", fontFamily: "monospace", marginBottom: 10 }}>{p.meta}</div>
                    <div style={{ fontSize: 14, color: "#c9d1d9", lineHeight: 1.7 }}>{p.desc}</div>
                  </div>
                ))}

                <hr style={{ border: "none", borderTop: "1px solid #21262d", marginBottom: 28, marginTop: 12 }} />

                {/* Currently Building */}
                <h2 style={{ fontSize: 18, fontWeight: 700, color: "#f0f6fc", marginBottom: 14 }}>🚧 Currently Building</h2>
                <div style={{ marginBottom: 28 }}>
                  {[
                    "SQL fundamentals — working through structured query practice daily",
                    "Power BI basics — moving dashboards beyond Excel",
                    "BA documentation skills — BRDs, user stories, process maps",
                    "90-day BA transition plan — building a portfolio to match the career pivot",
                  ].map((item, i) => (
                    <div key={i} style={{ display: "flex", gap: 10, marginBottom: 10, alignItems: "flex-start" }}>
                      <span style={{ color: "#f78166", marginTop: 2 }}>▸</span>
                      <span style={{ fontSize: 14, color: "#c9d1d9", lineHeight: 1.6 }}>{item}</span>
                    </div>
                  ))}
                </div>

                <hr style={{ border: "none", borderTop: "1px solid #21262d", marginBottom: 28 }} />

                {/* Contact */}
                <h2 style={{ fontSize: 18, fontWeight: 700, color: "#f0f6fc", marginBottom: 14 }}>📬 Reach Me</h2>
                <div style={{ display: "flex", flexDirection: "column", gap: 8, marginBottom: 24 }}>
                  {[
                    ["📧", "anneflora2003@gmail.com"],
                    ["💼", "linkedin.com/in/anneflora"],
                    ["📍", "Thiruvallur, Tamil Nadu"],
                  ].map(([icon, val], i) => (
                    <div key={i} style={{ fontSize: 14, color: "#c9d1d9" }}>
                      {icon} <span style={{ color: "#79c0ff" }}>{val}</span>
                    </div>
                  ))}
                </div>
                <div style={{
                  background: "#0d2818", border: "1px solid #238636",
                  borderRadius: 8, padding: "14px 18px",
                  fontSize: 13, color: "#3fb950", fontStyle: "italic",
                }}>
                  Open to entry-level BA or DA roles. If you're hiring for someone who can bridge operations and analysis — let's talk.
                </div>
              </div>
            </div>
          </div>
        )}

        {tab === "raw" && (
          <div>
            {/* Bio raw */}
            <div style={{
              background: "#161b22", border: "1px solid #21262d",
              borderRadius: 10, marginBottom: 20, overflow: "hidden",
            }}>
              <div style={{
                padding: "12px 20px", borderBottom: "1px solid #21262d",
                display: "flex", justifyContent: "space-between", alignItems: "center",
              }}>
                <span style={{ fontSize: 12, fontFamily: "monospace", color: "#8b949e" }}>GitHub Bio — paste into your profile settings</span>
                <button
                  onClick={() => copyText(bioText, "bio-raw")}
                  style={{
                    background: copied === "bio-raw" ? "#238636" : "#21262d",
                    border: "1px solid #30363d", borderRadius: 6,
                    color: "#f0f6fc", padding: "5px 12px", fontSize: 12,
                    fontFamily: "monospace", cursor: "pointer",
                  }}
                >{copied === "bio-raw" ? "✓ Copied" : "Copy"}</button>
              </div>
              <pre style={{
                margin: 0, padding: "20px",
                fontSize: 13, color: "#c9d1d9", fontFamily: "monospace",
                whiteSpace: "pre-wrap", lineHeight: 1.6,
                background: "#0d1117",
              }}>{bioText}</pre>
            </div>

            {/* README raw */}
            <div style={{
              background: "#161b22", border: "1px solid #21262d",
              borderRadius: 10, overflow: "hidden",
            }}>
              <div style={{
                padding: "12px 20px", borderBottom: "1px solid #21262d",
                display: "flex", justifyContent: "space-between", alignItems: "center",
              }}>
                <span style={{ fontSize: 12, fontFamily: "monospace", color: "#8b949e" }}>README.md — paste into AnneFlora/AnneFlora/README.md</span>
                <button
                  onClick={() => copyText(readmeRaw, "readme-raw")}
                  style={{
                    background: copied === "readme-raw" ? "#238636" : "#21262d",
                    border: "1px solid #30363d", borderRadius: 6,
                    color: "#f0f6fc", padding: "5px 12px", fontSize: 12,
                    fontFamily: "monospace", cursor: "pointer",
                  }}
                >{copied === "readme-raw" ? "✓ Copied" : "Copy README"}</button>
              </div>
              <pre style={{
                margin: 0, padding: "20px",
                fontSize: 12, color: "#c9d1d9", fontFamily: "monospace",
                whiteSpace: "pre-wrap", lineHeight: 1.7,
                background: "#0d1117",
                maxHeight: 600, overflowY: "auto",
              }}>{readmeRaw}</pre>
            </div>
          </div>
        )}

        {/* Footer note */}
        <div style={{
          marginTop: 24, padding: "16px 20px",
          background: "#161b22", border: "1px solid #21262d",
          borderRadius: 8, fontSize: 12,
          color: "#8b949e", fontFamily: "monospace",
          lineHeight: 1.6,
        }}>
          <span style={{ color: "#f78166" }}>→ How to use:</span> Switch to the <strong style={{ color: "#c9d1d9" }}>Raw</strong> tab to copy. Bio goes in GitHub Settings → Edit Profile → Bio. README goes into a repo named exactly <strong style={{ color: "#c9d1d9" }}>AnneFlora</strong> (same as your username) in a file called README.md.
        </div>
      </div>
    </div>
  );
}
