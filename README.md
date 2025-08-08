# Workspace
Public Workspace For Ideas 
import React from "react";
import { motion } from "framer-motion";
import { 
  Briefcase, TrendingUp, BarChart3, Cpu, Sparkles, Mail, Linkedin, FileText, ArrowRight, Target, Users, LineChart
} from "lucide-react";

// Tailwind is assumed available. Uses shadcn/ui primitives if your build has them installed.
// If not using shadcn, the Tailwind classes alone will render a clean UI.

export default function PortfolioLanding() {
  return (
    <main className="min-h-screen bg-neutral-50 text-neutral-900">
      {/* Hero */}
      <section className="relative overflow-hidden">
        <div className="absolute inset-0 bg-gradient-to-br from-indigo-50 via-white to-cyan-50" />
        <div className="relative mx-auto max-w-7xl px-6 py-20">
          <div className="grid grid-cols-1 gap-10 md:grid-cols-2 md:items-center">
            <motion.div initial={{ opacity: 0, y: 12 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }}>
              <div className="inline-flex items-center space-x-2 rounded-full bg-white/70 px-4 py-1 text-sm shadow-sm ring-1 ring-black/5">
                <Sparkles className="h-4 w-4" />
                <span>Analytics Leader • Retail Ops • AI-driven outcomes</span>
              </div>
              <h1 className="mt-6 text-4xl font-semibold tracking-tight sm:text-5xl">
                Jon Johnson
              </h1>
              <p className="mt-3 text-lg text-neutral-700">
                Director-level analytics and workforce reporting leader. I operationalize AI, automate insights, and translate complex data into decisions that move EBIT.
              </p>
              <div className="mt-8 flex flex-wrap gap-3">
                <a href="#contact" className="inline-flex items-center rounded-2xl bg-neutral-900 px-5 py-3 text-white shadow-sm transition hover:opacity-90">
                  <Mail className="mr-2 h-4 w-4" /> Contact
                </a>
                <a href="#projects" className="inline-flex items-center rounded-2xl bg-white px-5 py-3 text-neutral-900 shadow-sm ring-1 ring-neutral-200 transition hover:bg-neutral-50">
                  <ArrowRight className="mr-2 h-4 w-4" /> View Work
                </a>
                <a href="/Jon_Johnson_Resume.pdf" className="inline-flex items-center rounded-2xl bg-white px-5 py-3 text-neutral-900 shadow-sm ring-1 ring-neutral-200 transition hover:bg-neutral-50">
                  <FileText className="mr-2 h-4 w-4" /> Download Resume
                </a>
              </div>
            </motion.div>

            <motion.div initial={{ opacity: 0, y: 12 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6, delay: 0.1 }} className="">
              <div className="rounded-3xl bg-white p-6 shadow-sm ring-1 ring-neutral-200">
                <div className="grid grid-cols-3 gap-4">
                  {[
                    { label: "WFM reports automated", value: "150+", icon: BarChart3 },
                    { label: "Retail brands served", value: "4", icon: Briefcase },
                    { label: "Stakeholders enabled", value: "1.5k+", icon: Users },
                  ].map((kpi, i) => (
                    <div key={i} className="rounded-2xl bg-neutral-50 p-4 ring-1 ring-neutral-100">
                      <kpi.icon className="h-5 w-5" />
                      <div className="mt-3 text-2xl font-semibold">{kpi.value}</div>
                      <div className="text-sm text-neutral-600">{kpi.label}</div>
                    </div>
                  ))}
                </div>
                <div className="mt-6 grid grid-cols-2 gap-4">
                  <div className="rounded-2xl bg-gradient-to-br from-indigo-50 to-white p-4 ring-1 ring-indigo-100">
                    <div className="text-sm text-neutral-600">Core Focus</div>
                    <div className="mt-1 font-medium">Workforce analytics, Power BI, UKG, retail ops</div>
                  </div>
                  <div className="rounded-2xl bg-gradient-to-br from-cyan-50 to-white p-4 ring-1 ring-cyan-100">
                    <div className="text-sm text-neutral-600">Edge</div>
                    <div className="mt-1 font-medium">AI copilots that generate DAX and insights</div>
                  </div>
                </div>
              </div>
            </motion.div>
          </div>
        </div>
      </section>

      {/* Value props */}
      <section className="mx-auto max-w-7xl px-6 py-16" id="about">
        <div className="grid grid-cols-1 gap-6 md:grid-cols-3">
          {[
            {
              title: "Decision velocity",
              copy:
                "I build reporting ecosystems that compress time-to-insight for finance and ops leaders.",
              icon: TrendingUp,
            },
            {
              title: "AI at the core",
              copy:
                "Copilot agents, anomaly detection, and what-if modeling embedded where work happens.",
              icon: Cpu,
            },
            {
              title: "Outcomes",
              copy:
                "Labor productivity, forecast accuracy, and schedule adherence improvements that stick.",
              icon: Target,
            },
          ].map((v, i) => (
            <div key={i} className="rounded-3xl bg-white p-6 shadow-sm ring-1 ring-neutral-200">
              <v.icon className="h-6 w-6" />
              <h3 className="mt-4 text-xl font-semibold">{v.title}</h3>
              <p className="mt-2 text-neutral-700">{v.copy}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Experience timeline */}
      <section className="mx-auto max-w-7xl px-6 py-8" id="experience">
        <div className="mb-6 flex items-center gap-2">
          <Briefcase className="h-5 w-5" />
          <h2 className="text-2xl font-semibold">Experience</h2>
        </div>
        <div className="space-y-5">
          {[
            {
              role: "Reporting and Analytics • Finance Ops",
              company: "Gap Inc.",
              period: "2023 — Present",
              highlights: [
                "Co-led UKG Phase 3 Power BI rollout across brands",
                "Built labor dashboards for NSO and PSJ with automated store setup workflows",
                "Established WFM success metrics and anomaly alerts"
              ],
            },
            {
              role: "Workforce Analytics Lead",
              company: "Retail Portfolio",
              period: "2019 — 2023",
              highlights: [
                "Scaled cross-brand reporting with governance and SLAs",
                "Introduced metric spotlight pages and leader impact views",
                "Reduced manual reporting by 70% through automation"
              ],
            },
            {
              role: "Supply Chain Manager",
              company: "ESI",
              period: "2016 — 2019",
              highlights: [
                "Increased order fill rate via profitability-weighted allocation",
                "Improved contract margins by shipment consolidation",
                "Launched SKU test-and-scale framework to improve ROI"
              ],
            },
          ].map((job, i) => (
            <div key={i} className="rounded-3xl bg-white p-6 shadow-sm ring-1 ring-neutral-200">
              <div className="flex flex-wrap items-baseline justify-between gap-3">
                <div>
                  <div className="text-lg font-semibold">{job.role}</div>
                  <div className="text-neutral-600">{job.company}</div>
                </div>
                <div className="text-sm text-neutral-600">{job.period}</div>
              </div>
              <ul className="mt-4 list-disc space-y-2 pl-6 text-neutral-700">
                {job.highlights.map((h, idx) => (
                  <li key={idx}>{h}</li>
                ))}
              </ul>
            </div>
          ))}
        </div>
      </section>

      {/* Featured work */}
      <section className="mx-auto max-w-7xl px-6 py-8" id="projects">
        <div className="mb-6 flex items-center gap-2">
          <LineChart className="h-5 w-5" />
          <h2 className="text-2xl font-semibold">Featured Work</h2>
        </div>
        <div className="grid grid-cols-1 gap-6 md:grid-cols-3">
          {[
            {
              title: "WFM Copilot for Power BI",
              blurb:
                "Natural language to DAX, anomaly detection, viz suggestions, and what-if analysis for labor KPIs.",
              tags: ["Power BI", "Copilot Studio", "DAX", "UKG"],
              link: "#",
            },
            {
              title: "Text-to-Learning SaaS",
              blurb:
                "Transforms raw content into learning modules with quizzes and adaptive paths.",
              tags: ["Next.js", "FastAPI", "OpenAI", "Stripe"],
              link: "#",
            },
            {
              title: "Church Engagement Risk Scoring",
              blurb:
                "Predicts disengagement risk and prescribes outreach actions for ministry teams.",
              tags: ["Classification", "Airtable", "LLM", "n8n"],
              link: "#",
            },
          ].map((p, i) => (
            <a key={i} href={p.link} className="group rounded-3xl bg-white p-6 shadow-sm ring-1 ring-neutral-200 transition hover:shadow-md">
              <div className="text-lg font-semibold group-hover:underline">{p.title}</div>
              <p className="mt-2 text-neutral-700">{p.blurb}</p>
              <div className="mt-4 flex flex-wrap gap-2">
                {p.tags.map((t, idx) => (
                  <span key={idx} className="rounded-full bg-neutral-100 px-3 py-1 text-xs text-neutral-700 ring-1 ring-neutral-200">
                    {t}
                  </span>
                ))}
              </div>
            </a>
          ))}
        </div>
      </section>

      {/* Testimonials */}
      <section className="mx-auto max-w-7xl px-6 py-8" id="testimonials">
        <div className="rounded-3xl bg-gradient-to-br from-neutral-900 to-neutral-800 p-8 text-white">
          <div className="grid grid-cols-1 gap-6 md:grid-cols-3">
            {[
              {
                quote:
                  "Jon translates business noise into a crisp analytics roadmap that leaders can execute against.",
                name: "SVP, Retail Operations",
              },
              {
                quote:
                  "The WFM Copilot changed how our managers engage with labor metrics. Real adoption, real results.",
                name: "Director, Workforce Management",
              },
              {
                quote:
                  "Fast, pragmatic, and enterprise-ready. Automations reduced manual reporting by more than half.",
                name: "Finance Transformation Lead",
              },
            ].map((t, i) => (
              <div key={i} className="rounded-2xl bg-white/5 p-6 ring-1 ring-white/10">
                <p className="text-sm leading-relaxed opacity-90">“{t.quote}”</p>
                <div className="mt-4 text-xs opacity-70">{t.name}</div>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="mx-auto max-w-7xl px-6 py-16">
        <div className="rounded-3xl bg-white p-8 shadow-sm ring-1 ring-neutral-200">
          <h2 className="text-2xl font-semibold">Let’s connect</h2>
          <p className="mt-2 max-w-3xl text-neutral-700">
            I partner with executives and product teams to unlock decision velocity. If you are exploring advanced reporting, AI copilots, or retail workforce outcomes, reach out.
          </p>
          <div className="mt-6 flex flex-wrap gap-3">
            <a href="mailto:jon@example.com" className="inline-flex items-center rounded-2xl bg-neutral-900 px-5 py-3 text-white shadow-sm transition hover:opacity-90">
              <Mail className="mr-2 h-4 w-4" /> jon@example.com
            </a>
            <a href="https://www.linkedin.com/in/johnson689/" target="_blank" rel="noreferrer" className="inline-flex items-center rounded-2xl bg-white px-5 py-3 text-neutral-900 shadow-sm ring-1 ring-neutral-200 transition hover:bg-neutral-50">
              <Linkedin className="mr-2 h-4 w-4" /> LinkedIn
            </a>
          </div>
        </div>
      </section>

      <footer className="mx-auto max-w-7xl px-6 pb-14 text-sm text-neutral-600">
        © {new Date().getFullYear()} Jon Johnson. All rights reserved.
      </footer>
    </main>
  );
}
