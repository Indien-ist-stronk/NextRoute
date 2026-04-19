import React, { useMemo, useState } from "react";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Progress } from "@/components/ui/progress";
import { Badge } from "@/components/ui/badge";
import { RadioGroup, RadioGroupItem } from "@/components/ui/radio-group";
import { Label } from "@/components/ui/label";
import { Textarea } from "@/components/ui/textarea";
import { motion, AnimatePresence } from "framer-motion";
import { Brain, ChevronRight, RotateCcw, Target, BarChart3, Sparkles, ShieldCheck } from "lucide-react";

const DOMAIN_META = {
  tech: {
    label: "Tech / Computer Science",
    cluster: "Analytical",
    description: "Strong fit for coding, systems thinking, automation, software products, and AI-oriented paths.",
    nextSteps: [
      "Build one tiny app, calculator, or quiz website in the next 7 days.",
      "Try a beginner Python or JavaScript course and finish at least one project.",
      "Speak to a university student or mentor in CS, AI, or software engineering."
    ],
    courses: ["Computer Science", "AI & Data Science", "Software Engineering", "Cybersecurity"]
  },
  science: {
    label: "Pure Science",
    cluster: "Analytical",
    description: "Strong fit for theory, curiosity, experimentation, research, and deep conceptual understanding.",
    nextSteps: [
      "Choose one science topic and create a 1-page research summary.",
      "Join or watch a science competition, Olympiad, or lab-based project.",
      "Explore university majors like physics, chemistry, biology, or biotechnology."
    ],
    courses: ["Physics", "Chemistry", "Biology", "Biotechnology", "Environmental Science"]
  },
  engineering: {
    label: "Engineering",
    cluster: "Analytical",
    description: "Strong fit for applied problem-solving, practical systems, design under constraints, and building solutions.",
    nextSteps: [
      "Build or design one simple prototype, model, or technical concept.",
      "Explore branches like mechanical, civil, electrical, robotics, or mechatronics.",
      "Try a project where you solve a real-world problem with a working design."
    ],
    courses: ["Mechanical Engineering", "Electrical Engineering", "Civil Engineering", "Robotics", "Mechatronics"]
  },
  medicine: {
    label: "Medicine / Health Sciences",
    cluster: "People-Centric",
    description: "Strong fit for patient care, responsibility, biological sciences, and long-term professional commitment.",
    nextSteps: [
      "Shadow, observe, or interview someone in healthcare if possible.",
      "Explore medicine, dentistry, pharmacy, physiotherapy, and biomedical pathways.",
      "Check whether you can sustain long study duration and high responsibility."
    ],
    courses: ["Medicine", "Dentistry", "Pharmacy", "Physiotherapy", "Biomedical Sciences"]
  },
  psychology: {
    label: "Psychology / Behavioral Sciences",
    cluster: "People-Centric",
    description: "Strong fit for understanding emotions, behavior, patterns of thinking, and supportive human-focused work.",
    nextSteps: [
      "Read introductory psychology material and summarize one concept clearly.",
      "Observe whether you genuinely like listening, understanding, and pattern-spotting in people.",
      "Explore psychology, counseling-related tracks, behavioral science, and neuroscience pathways."
    ],
    courses: ["Psychology", "Behavioral Science", "Neuroscience", "Cognitive Science"]
  },
  education: {
    label: "Education / Teaching",
    cluster: "People-Centric",
    description: "Strong fit for explanation, mentoring, clarity-building, and helping others learn step by step.",
    nextSteps: [
      "Teach one concept to juniors and check whether you enjoy the process.",
      "Create one explainer note, short tutorial, or slide deck on a topic you know.",
      "Explore education, instructional design, academic mentoring, and teaching careers."
    ],
    courses: ["Education", "Early Childhood Education", "Special Education", "Instructional Design"]
  },
  law: {
    label: "Law",
    cluster: "People-Centric",
    description: "Strong fit for argument, interpretation, language precision, structured reasoning, and advocacy.",
    nextSteps: [
      "Write a 500-word argument on a current issue from two sides.",
      "Try debate, model UN, policy writing, or public speaking activities.",
      "Explore law, public policy, international relations, and legal studies pathways."
    ],
    courses: ["Law", "Legal Studies", "Public Policy", "International Relations"]
  },
  arts: {
    label: "Fine Arts / Creative Fields",
    cluster: "Creative / Strategic",
    description: "Strong fit for expression, originality, storytelling, aesthetic thinking, and creative experimentation.",
    nextSteps: [
      "Create one real portfolio piece this week: design, writing, music, film, or art.",
      "Check whether you enjoy creating repeatedly, not only imagining.",
      "Explore fine arts, media, visual communication, animation, or creative writing."
    ],
    courses: ["Fine Arts", "Media Studies", "Animation", "Creative Writing", "Film"]
  },
  design: {
    label: "Design / Architecture",
    cluster: "Creative / Strategic",
    description: "Strong fit for visual thinking, structure plus aesthetics, iteration, and turning ideas into designed experiences or spaces.",
    nextSteps: [
      "Create one design sample: poster, interface, room layout, product sketch, or 3D idea.",
      "Explore design tools and basic principles of layout, function, and form.",
      "Compare architecture, product design, UI/UX, and visual design pathways."
    ],
    courses: ["Architecture", "Product Design", "UI/UX Design", "Interior Design", "Visual Communication"]
  },
  commerce: {
    label: "Commerce / Business",
    cluster: "Creative / Strategic",
    description: "Strong fit for value creation, strategy, decision-making, markets, enterprise, and resource allocation.",
    nextSteps: [
      "Plan a tiny business idea or school initiative with cost, pricing, and value proposition.",
      "Explore finance, accounting, management, economics, and entrepreneurship.",
      "Test whether you enjoy decision-making under uncertainty and competition."
    ],
    courses: ["Business Administration", "Finance", "Economics", "Accounting", "Entrepreneurship"]
  },
  social: {
    label: "Social Sciences",
    cluster: "People-Centric",
    description: "Strong fit for studying society, culture, systems, communities, and real-world human issues at scale.",
    nextSteps: [
      "Choose a social issue and analyze causes, stakeholders, and possible solutions.",
      "Explore sociology, political science, anthropology, development studies, and economics-social policy intersections.",
      "Check whether you prefer understanding systems of society over one-to-one helping roles."
    ],
    courses: ["Sociology", "Political Science", "Anthropology", "Development Studies", "Public Administration"]
  }
};

const CLUSTERS = {
  analytical: ["tech", "science", "engineering"],
  people: ["medicine", "psychology", "education", "law", "social"],
  creative: ["arts", "design", "commerce"]
};

const QUESTIONS = {
  broad: [
    {
      id: "b1",
      text: "Which type of work naturally pulls you in the most?",
      options: [
        { label: "Solving logical or technical problems", scores: { tech: 2, science: 1, engineering: 1 }, nextCluster: "analytical" },
        { label: "Working directly with people and their needs", scores: { medicine: 1, psychology: 1, education: 1, law: 1, social: 1 }, nextCluster: "people" },
        { label: "Creating, designing, planning, or building ideas into something visible", scores: { arts: 1, design: 2, commerce: 1 }, nextCluster: "creative" }
      ]
    },
    {
      id: "b2",
      text: "Which kind of satisfaction feels strongest to you?",
      options: [
        { label: "A system works efficiently because I figured it out", scores: { tech: 2, engineering: 1, commerce: 1 } },
        { label: "I understood something deeply that others missed", scores: { science: 2, psychology: 1, social: 1 } },
        { label: "I helped, influenced, taught, or guided people meaningfully", scores: { medicine: 1, education: 2, law: 1, psychology: 1, social: 1 } },
        { label: "I created something original, elegant, or impactful", scores: { arts: 2, design: 2, commerce: 1 } }
      ]
    },
    {
      id: "b3",
      text: "Which type of challenge would you willingly tolerate again and again?",
      options: [
        { label: "Debugging, testing, and solving technical errors", scores: { tech: 2, engineering: 1 } },
        { label: "Studying complex ideas for a long time", scores: { science: 2, medicine: 1, law: 1 } },
        { label: "People pressure, responsibility, or emotional complexity", scores: { medicine: 2, psychology: 2, education: 1, law: 1, social: 1 } },
        { label: "Competition, uncertainty, repeated iteration, or subjective judgment", scores: { arts: 1, design: 2, commerce: 2 } }
      ]
    }
  ],
  analytical: [
    {
      id: "a1",
      text: "Which one excites you most?",
      options: [
        { label: "Writing code, automating, or building digital tools", scores: { tech: 3 } },
        { label: "Understanding why a phenomenon exists", scores: { science: 3 } },
        { label: "Designing a real-world solution that works", scores: { engineering: 3 } }
      ]
    },
    {
      id: "a2",
      text: "Pick the 6-month project you would most likely finish strongly.",
      options: [
        { label: "Build an app or software tool", scores: { tech: 3, engineering: 1 } },
        { label: "Do a research project and analyze findings", scores: { science: 3 } },
        { label: "Create a product or solve a practical technical problem", scores: { engineering: 3, tech: 1 } }
      ]
    },
    {
      id: "a3",
      text: "Which statement sounds most like you?",
      options: [
        { label: "I enjoy systems, logic, and digital creation", scores: { tech: 3 } },
        { label: "I enjoy theory, curiosity, and discovering how things work at a deep level", scores: { science: 3 } },
        { label: "I enjoy applying knowledge to practical, constrained problems", scores: { engineering: 3 } }
      ]
    },
    {
      id: "a4",
      text: "Forced choice: which is more satisfying?",
      options: [
        { label: "A working software solution", scores: { tech: 2 } },
        { label: "A correct explanation of a natural phenomenon", scores: { science: 2 } },
        { label: "A functional design that solves a real need", scores: { engineering: 2 } }
      ]
    }
  ],
  people: [
    {
      id: "p1",
      text: "Which role feels most natural to you?",
      options: [
        { label: "Treating physical health needs", scores: { medicine: 3 } },
        { label: "Understanding emotions and behavior", scores: { psychology: 3 } },
        { label: "Explaining clearly and helping others learn", scores: { education: 3 } },
        { label: "Arguing, interpreting, and defending positions", scores: { law: 3 } },
        { label: "Studying society, policy, and large human systems", scores: { social: 3 } }
      ]
    },
    {
      id: "p2",
      text: "Choose the project you would most likely complete well.",
      options: [
        { label: "Observe, support, or explore healthcare-related work", scores: { medicine: 3 } },
        { label: "Analyze why people think, feel, or behave in certain ways", scores: { psychology: 3 } },
        { label: "Teach a concept or mentor younger students", scores: { education: 3 } },
        { label: "Research a public issue and argue a position", scores: { law: 3, social: 1 } },
        { label: "Study a community problem and propose system-level solutions", scores: { social: 3, law: 1 } }
      ]
    },
    {
      id: "p3",
      text: "Which type of effort can you tolerate for years?",
      options: [
        { label: "Long study and high responsibility", scores: { medicine: 3 } },
        { label: "Listening deeply and carrying emotional complexity", scores: { psychology: 3 } },
        { label: "Repeating explanations until others understand", scores: { education: 3 } },
        { label: "Conflict, debate, and pressure to defend arguments", scores: { law: 3 } },
        { label: "Ambiguity in social systems and public issues", scores: { social: 3 } }
      ]
    },
    {
      id: "p4",
      text: "Forced choice: what gives you stronger satisfaction?",
      options: [
        { label: "Helping one person directly", scores: { medicine: 2, psychology: 1 } },
        { label: "Changing how people understand something", scores: { education: 2, law: 1 } },
        { label: "Understanding society and influencing larger systems", scores: { social: 2, law: 1 } },
        { label: "Making a strong case with logic and language", scores: { law: 2 } }
      ]
    }
  ],
  creative: [
    {
      id: "c1",
      text: "Which direction fits best?",
      options: [
        { label: "Expressing ideas, stories, visuals, or emotions creatively", scores: { arts: 3 } },
        { label: "Designing spaces, products, interfaces, or structured visuals", scores: { design: 3 } },
        { label: "Building value through strategy, money, markets, or enterprise", scores: { commerce: 3 } }
      ]
    },
    {
      id: "c2",
      text: "Choose the project you would most likely sustain for 6 months.",
      options: [
        { label: "Create a portfolio of art, media, writing, film, or music", scores: { arts: 3 } },
        { label: "Design a product, building concept, interface, or visual system", scores: { design: 3 } },
        { label: "Launch a mini venture or business concept", scores: { commerce: 3 } }
      ]
    },
    {
      id: "c3",
      text: "Which trade-off are you most willing to accept?",
      options: [
        { label: "Subjective feedback and creative uncertainty", scores: { arts: 3 } },
        { label: "Repeated iteration to balance beauty and function", scores: { design: 3 } },
        { label: "Competition, risk, and decision pressure", scores: { commerce: 3 } }
      ]
    },
    {
      id: "c4",
      text: "Forced choice: which is more satisfying?",
      options: [
        { label: "A unique creative output", scores: { arts: 2 } },
        { label: "A clean, effective design", scores: { design: 2 } },
        { label: "A strategy that creates measurable value", scores: { commerce: 2 } }
      ]
    }
  ],
  cross: [
    {
      id: "x1",
      text: "In the last 6 months, what have you actually done most consistently?",
      options: [
        { label: "Built or explored tech tools, coding, or digital systems", scores: { tech: 3 } },
        { label: "Read deeply, researched topics, or explored scientific ideas", scores: { science: 3 } },
        { label: "Built, fixed, or designed practical solutions", scores: { engineering: 3 } },
        { label: "Helped people in health, care, or biology-related interests", scores: { medicine: 3 } },
        { label: "Listened to problems, reflected on behavior, or explored the mind", scores: { psychology: 3 } },
        { label: "Explained concepts, guided classmates, or taught others", scores: { education: 3 } },
        { label: "Debated, argued, or followed legal/social issues", scores: { law: 3, social: 1 } },
        { label: "Created art, media, writing, or expressive work", scores: { arts: 3 } },
        { label: "Designed layouts, visuals, interfaces, or spatial ideas", scores: { design: 3 } },
        { label: "Planned business ideas, pricing, value, or strategy", scores: { commerce: 3 } },
        { label: "Analyzed society, communities, or public issues", scores: { social: 3 } }
      ]
    },
    {
      id: "x2",
      text: "Which type of university workload sounds most sustainable for you?",
      options: [
        { label: "Projects, systems, logic, and technical problem-solving", scores: { tech: 2, engineering: 2 } },
        { label: "Deep reading, theory, and research", scores: { science: 2, law: 1, social: 1 } },
        { label: "Long study with human responsibility", scores: { medicine: 2, psychology: 1, education: 1 } },
        { label: "Creative portfolio work and iteration", scores: { arts: 2, design: 2 } },
        { label: "Strategy, markets, decisions, and uncertainty", scores: { commerce: 2 } }
      ]
    },
    {
      id: "x3",
      text: "Which statement best describes your strongest edge?",
      options: [
        { label: "I think logically and like systems", scores: { tech: 2, engineering: 1 } },
        { label: "I am deeply curious and like understanding why things happen", scores: { science: 2 } },
        { label: "I can stay calm with responsibility and people", scores: { medicine: 2, psychology: 1, education: 1 } },
        { label: "I use language, explanation, or argument strongly", scores: { law: 2, education: 1, social: 1 } },
        { label: "I notice form, aesthetics, and original expression", scores: { arts: 2, design: 2 } },
        { label: "I notice opportunity, value, and decisions", scores: { commerce: 2 } }
      ]
    },
    {
      id: "x4",
      text: "Which type of future role sounds closest to your natural direction?",
      options: [
        { label: "Builder of digital systems", scores: { tech: 2 } },
        { label: "Researcher or scientist", scores: { science: 2 } },
        { label: "Problem-solving engineer", scores: { engineering: 2 } },
        { label: "Healthcare professional", scores: { medicine: 2 } },
        { label: "Behavior or people specialist", scores: { psychology: 2 } },
        { label: "Teacher, explainer, or mentor", scores: { education: 2 } },
        { label: "Law, advocacy, or policy professional", scores: { law: 2, social: 1 } },
        { label: "Artist, media creator, or storyteller", scores: { arts: 2 } },
        { label: "Designer or architect", scores: { design: 2 } },
        { label: "Business, finance, or entrepreneurship professional", scores: { commerce: 2 } },
        { label: "Social systems or public impact professional", scores: { social: 2 } }
      ]
    }
  ],
  impact: [
    {
      id: "i1",
      text: "Before this assessment, how much career clarity did you have?",
      options: [
        { label: "High clarity", valueOnly: "high" },
        { label: "Some clarity", valueOnly: "some" },
        { label: "Low clarity", valueOnly: "low" }
      ]
    },
    {
      id: "i2",
      text: "After this assessment, do you feel clearer about your direction?",
      options: [
        { label: "Yes, much clearer", valueOnly: "high" },
        { label: "Somewhat clearer", valueOnly: "some" },
        { label: "Not really", valueOnly: "low" }
      ]
    },
    {
      id: "i3",
      text: "Will you explore the suggested direction further?",
      options: [
        { label: "Yes", valueOnly: "yes" },
        { label: "Maybe", valueOnly: "maybe" },
        { label: "No", valueOnly: "no" }
      ]
    }
  ]
};

function normalizeScores(scores) {
  const max = Math.max(...Object.values(scores), 1);
  const result = {};
  Object.entries(scores).forEach(([k, v]) => {
    result[k] = Math.round((v / max) * 100);
  });
  return result;
}

function sortDomains(scores) {
  return Object.entries(scores).sort((a, b) => b[1] - a[1]);
}

function mergeScores(prev, next) {
  const merged = { ...prev };
  Object.entries(next || {}).forEach(([k, v]) => {
    merged[k] = (merged[k] || 0) + v;
  });
  return merged;
}

function getLikelyCluster(scores) {
  const sums = {
    analytical: CLUSTERS.analytical.reduce((acc, d) => acc + (scores[d] || 0), 0),
    people: CLUSTERS.people.reduce((acc, d) => acc + (scores[d] || 0), 0),
    creative: CLUSTERS.creative.reduce((acc, d) => acc + (scores[d] || 0), 0)
  };
  return Object.entries(sums).sort((a, b) => b[1] - a[1])[0][0];
}

function buildResults(scores, freeText) {
  const normalized = normalizeScores(scores);
  const ranked = sortDomains(normalized);
  const top3 = ranked.slice(0, 3).map(([key, score]) => ({ key, score, ...DOMAIN_META[key] }));
  const primary = top3[0];
  const secondary = top3[1];
  const tertiary = top3[2];
  const recommendationText = `You show the strongest alignment with ${primary.label}. ${secondary ? `Your next closest match is ${secondary.label}. ` : ""}${tertiary ? `A third adjacent direction is ${tertiary.label}.` : ""}`;

  const explanation = [
    `Primary cluster: ${DOMAIN_META[primary.key].cluster}`,
    `${primary.label} stands out because your pattern suggests repeatable motivation, fit with its workload, and tolerance for its core challenges.`
  ];

  if (freeText) {
    explanation.push(`Your own reflection also adds context: "${freeText}"`);
  }

  return { normalized, top3, recommendationText, explanation };
}

function saveAnonymousAnalytics(payload) {
  try {
    const existing = JSON.parse(localStorage.getItem("career_assessment_analytics") || "[]");
    existing.push({ ...payload, timestamp: new Date().toISOString() });
    localStorage.setItem("career_assessment_analytics", JSON.stringify(existing));
  } catch (e) {
    console.error("Analytics save failed", e);
  }
}

export default function CareerDirectionAdaptiveApp() {
  const [started, setStarted] = useState(false);
  const [stepIndex, setStepIndex] = useState(0);
  const [stage, setStage] = useState("broad");
  const [answers, setAnswers] = useState({});
  const [scores, setScores] = useState({
    tech: 0,
    science: 0,
    engineering: 0,
    medicine: 0,
    psychology: 0,
    education: 0,
    law: 0,
    arts: 0,
    design: 0,
    commerce: 0,
    social: 0
  });
  const [branch, setBranch] = useState(null);
  const [selected, setSelected] = useState("");
  const [clarityBefore, setClarityBefore] = useState("");
  const [clarityAfter, setClarityAfter] = useState("");
  const [exploreFurther, setExploreFurther] = useState("");
  const [reflection, setReflection] = useState("");
  const [finished, setFinished] = useState(false);

  const currentQuestionSet = stage === "broad"
    ? QUESTIONS.broad
    : stage === "branch"
      ? QUESTIONS[branch]
      : stage === "cross"
        ? QUESTIONS.cross
        : QUESTIONS.impact;

  const currentQuestion = currentQuestionSet[stepIndex];

  const totalSteps = QUESTIONS.broad.length + 4 + QUESTIONS.cross.length + QUESTIONS.impact.length;
  const progress = finished
    ? 100
    : Math.round(((Object.keys(answers).length + (clarityBefore ? 1 : 0) + (clarityAfter ? 1 : 0) + (exploreFurther ? 1 : 0)) / totalSteps) * 100);

  const results = useMemo(() => buildResults(scores, reflection), [scores, reflection]);

  function handleAnswer(option) {
    setAnswers((prev) => ({ ...prev, [currentQuestion.id]: option.label }));
    setScores((prev) => mergeScores(prev, option.scores));

    if (stage === "broad" && currentQuestion.id === "b1" && option.nextCluster) {
      setBranch(option.nextCluster);
    }

    setSelected("");

    const lastIndex = currentQuestionSet.length - 1;
    if (stepIndex < lastIndex) {
      setStepIndex(stepIndex + 1);
      return;
    }

    if (stage === "broad") {
      const chosenBranch = branch || option.nextCluster || getLikelyCluster(mergeScores(scores, option.scores));
      setBranch(chosenBranch);
      setStage("branch");
      setStepIndex(0);
      return;
    }

    if (stage === "branch") {
      setStage("cross");
      setStepIndex(0);
      return;
    }

    if (stage === "cross") {
      setStage("impact");
      setStepIndex(0);
      return;
    }

    if (stage === "impact") {
      setFinished(true);
    }
  }

  function handleImpactAnswer(option) {
    setAnswers((prev) => ({ ...prev, [currentQuestion.id]: option.label }));
    if (currentQuestion.id === "i1") setClarityBefore(option.valueOnly);
    if (currentQuestion.id === "i2") setClarityAfter(option.valueOnly);
    if (currentQuestion.id === "i3") setExploreFurther(option.valueOnly);

    setSelected("");

    const lastIndex = QUESTIONS.impact.length - 1;
    if (stepIndex < lastIndex) {
      setStepIndex(stepIndex + 1);
      return;
    }

    const payload = {
      primary: results.top3[0]?.key,
      secondary: results.top3[1]?.key,
      tertiary: results.top3[2]?.key,
      clarityBefore: currentQuestion.id === "i1" ? option.valueOnly : clarityBefore,
      clarityAfter: currentQuestion.id === "i2" ? option.valueOnly : clarityAfter,
      exploreFurther: currentQuestion.id === "i3" ? option.valueOnly : exploreFurther,
      normalizedScores: results.normalized
    };
    saveAnonymousAnalytics(payload);
    setFinished(true);
  }

  function resetAll() {
    setStarted(false);
    setStepIndex(0);
    setStage("broad");
    setAnswers({});
    setScores({
      tech: 0,
      science: 0,
      engineering: 0,
      medicine: 0,
      psychology: 0,
      education: 0,
      law: 0,
      arts: 0,
      design: 0,
      commerce: 0,
      social: 0
    });
    setBranch(null);
    setSelected("");
    setClarityBefore("");
    setClarityAfter("");
    setExploreFurther("");
    setReflection("");
    setFinished(false);
  }

  return (
    <div className="min-h-screen bg-background p-4 md:p-8">
      <div className="mx-auto max-w-5xl space-y-6">
        <motion.div
          initial={{ opacity: 0, y: 12 }}
          animate={{ opacity: 1, y: 0 }}
          className="grid gap-4 md:grid-cols-[1.4fr_0.8fr]"
        >
          <Card className="rounded-2xl shadow-sm">
            <CardHeader>
              <div className="flex items-center gap-3">
                <div className="rounded-2xl border p-2">
                  <Brain className="h-6 w-6" />
                </div>
                <div>
                  <CardTitle className="text-2xl">Adaptive Career Direction Assessment</CardTitle>
                  <p className="text-sm text-muted-foreground mt-1">
                    A student-friendly web app to identify stronger university direction patterns using adaptive questions, scoring, and action-based recommendations.
                  </p>
                </div>
              </div>
            </CardHeader>
            <CardContent className="space-y-4">
              <div className="flex flex-wrap gap-2">
                <Badge variant="secondary">Adaptive Flow</Badge>
                <Badge variant="secondary">Anonymous Analytics</Badge>
                <Badge variant="secondary">Career Recommendations</Badge>
                <Badge variant="secondary">Grade 11 Friendly</Badge>
              </div>
              <div className="grid gap-3 md:grid-cols-3">
                <div className="rounded-2xl border p-4">
                  <Target className="h-5 w-5 mb-2" />
                  <p className="font-medium">Targeted branching</p>
                  <p className="text-sm text-muted-foreground">The app changes question flow based on initial answers.</p>
                </div>
                <div className="rounded-2xl border p-4">
                  <Sparkles className="h-5 w-5 mb-2" />
                  <p className="font-medium">Action recommendations</p>
                  <p className="text-sm text-muted-foreground">Each result includes next steps and matching degree options.</p>
                </div>
                <div className="rounded-2xl border p-4">
                  <ShieldCheck className="h-5 w-5 mb-2" />
                  <p className="font-medium">Privacy-aware</p>
                  <p className="text-sm text-muted-foreground">No personal identifiers are required; analytics can stay anonymous.</p>
                </div>
              </div>
            </CardContent>
          </Card>

          <Card className="rounded-2xl shadow-sm">
            <CardHeader>
              <CardTitle className="text-lg">How it works</CardTitle>
            </CardHeader>
            <CardContent className="space-y-3 text-sm text-muted-foreground">
              <p>1. Broad questions identify a likely cluster.</p>
              <p>2. The app branches into a more specific stream path.</p>
              <p>3. Cross-validation checks real behavior and fit.</p>
              <p>4. The result shows top directions, explanations, and next steps.</p>
              <p>5. Anonymous impact data can be stored locally now, then later upgraded to Firebase or Supabase.</p>
            </CardContent>
          </Card>
        </motion.div>

        {started && !finished && (
          <Card className="rounded-2xl shadow-sm">
            <CardContent className="pt-6 space-y-3">
              <div className="flex items-center justify-between text-sm">
                <span>Progress</span>
                <span>{progress}%</span>
              </div>
              <Progress value={progress} />
            </CardContent>
          </Card>
        )}

        <AnimatePresence mode="wait">
          {!started ? (
            <motion.div
              key="start"
              initial={{ opacity: 0, y: 12 }}
              animate={{ opacity: 1, y: 0 }}
              exit={{ opacity: 0, y: -12 }}
            >
              <Card className="rounded-2xl shadow-sm">
                <CardContent className="pt-6 space-y-5">
                  <div>
                    <h2 className="text-xl font-semibold">Before students begin</h2>
                    <p className="text-sm text-muted-foreground mt-2">
                      This tool guides direction. It does not decide a career with absolute certainty. It works best as an early decision-support system and should be paired with real-world exploration.
                    </p>
                  </div>

                  <div className="rounded-2xl border p-4">
                    <p className="font-medium mb-2">Suggested instructions</p>
                    <ul className="list-disc pl-5 space-y-1 text-sm text-muted-foreground">
                      <li>Answer honestly based on what you would sustain, not what sounds impressive.</li>
                      <li>Choose what fits your repeated behavior, not your ideal self.</li>
                      <li>No names or email addresses are required.</li>
                    </ul>
                  </div>

                  <Button onClick={() => setStarted(true)} className="rounded-2xl">
                    Start Assessment <ChevronRight className="ml-2 h-4 w-4" />
                  </Button>
                </CardContent>
              </Card>
            </motion.div>
          ) : !finished ? (
            <motion.div
              key={`${stage}-${stepIndex}`}
              initial={{ opacity: 0, y: 12 }}
              animate={{ opacity: 1, y: 0 }}
              exit={{ opacity: 0, y: -12 }}
            >
              <Card className="rounded-2xl shadow-sm">
                <CardHeader>
                  <CardTitle className="text-xl">{currentQuestion?.text}</CardTitle>
                  <p className="text-sm text-muted-foreground">
                    {stage === "broad" && "Initial classification"}
                    {stage === "branch" && `Focused branch: ${branch === "analytical" ? "Analytical" : branch === "people" ? "People-Centric" : "Creative / Strategic"}`}
                    {stage === "cross" && "Cross-validation and fit check"}
                    {stage === "impact" && "Anonymous impact tracking"}
                  </p>
                </CardHeader>
                <CardContent className="space-y-5">
                  <RadioGroup value={selected} onValueChange={setSelected} className="space-y-3">
                    {currentQuestion?.options.map((option) => (
                      <div key={option.label} className="flex items-start space-x-3 rounded-2xl border p-4">
                        <RadioGroupItem value={option.label} id={option.label} className="mt-1" />
                        <Label htmlFor={option.label} className="cursor-pointer text-sm leading-6">
                          {option.label}
                        </Label>
                      </div>
                    ))}
                  </RadioGroup>

                  {stage === "cross" && currentQuestion?.id === "x4" && (
                    <div className="space-y-2">
                      <Label htmlFor="reflection">Optional reflection: what made you choose that?</Label>
                      <Textarea
                        id="reflection"
                        placeholder="Write a short sentence about what feels most natural to you..."
                        value={reflection}
                        onChange={(e) => setReflection(e.target.value)}
                        className="min-h-[100px] rounded-2xl"
                      />
                    </div>
                  )}

                  <Button
                    className="rounded-2xl"
                    disabled={!selected}
                    onClick={() => {
                      const option = currentQuestion.options.find((o) => o.label === selected);
                      if (!option) return;
                      if (stage === "impact") {
                        handleImpactAnswer(option);
                      } else {
                        handleAnswer(option);
                      }
                    }}
                  >
                    Continue <ChevronRight className="ml-2 h-4 w-4" />
                  </Button>
                </CardContent>
              </Card>
            </motion.div>
          ) : (
            <motion.div
              key="results"
              initial={{ opacity: 0, y: 12 }}
              animate={{ opacity: 1, y: 0 }}
            >
              <div className="grid gap-6 lg:grid-cols-[1.2fr_0.8fr]">
                <Card className="rounded-2xl shadow-sm">
                  <CardHeader>
                    <div className="flex items-center gap-3">
                      <BarChart3 className="h-6 w-6" />
                      <div>
                        <CardTitle className="text-2xl">Your adaptive result</CardTitle>
                        <p className="text-sm text-muted-foreground mt-1">This is a directional recommendation, not a final life decision.</p>
                      </div>
                    </div>
                  </CardHeader>
                  <CardContent className="space-y-6">
                    <div className="rounded-2xl border p-5">
                      <p className="text-sm text-muted-foreground">Primary match</p>
                      <h2 className="text-2xl font-semibold mt-1">{results.top3[0]?.label}</h2>
                      <p className="text-sm text-muted-foreground mt-2">{results.top3[0]?.description}</p>
                      <Badge className="mt-3 rounded-xl">Match score: {results.top3[0]?.score}%</Badge>
                    </div>

                    <div className="grid gap-4 md:grid-cols-3">
                      {results.top3.map((item, idx) => (
                        <div key={item.key} className="rounded-2xl border p-4">
                          <p className="text-xs uppercase tracking-wide text-muted-foreground">{idx === 0 ? "Primary" : idx === 1 ? "Secondary" : "Third"}</p>
                          <p className="font-medium mt-2">{item.label}</p>
                          <p className="text-sm text-muted-foreground mt-2">{item.score}% fit</p>
                        </div>
                      ))}
                    </div>

                    <div>
                      <h3 className="font-semibold mb-2">Why this result</h3>
                      <div className="space-y-2 text-sm text-muted-foreground">
                        {results.explanation.map((line) => (
                          <p key={line}>{line}</p>
                        ))}
                      </div>
                    </div>

                    <div>
                      <h3 className="font-semibold mb-2">Suggested university directions</h3>
                      <div className="flex flex-wrap gap-2">
                        {results.top3.flatMap((item) => item.courses.slice(0, 2)).slice(0, 6).map((course) => (
                          <Badge key={course} variant="secondary" className="rounded-xl">{course}</Badge>
                        ))}
                      </div>
                    </div>
                  </CardContent>
                </Card>

                <div className="space-y-6">
                  <Card className="rounded-2xl shadow-sm">
                    <CardHeader>
                      <CardTitle className="text-lg">Recommended next steps</CardTitle>
                    </CardHeader>
                    <CardContent>
                      <ol className="list-decimal pl-5 space-y-2 text-sm text-muted-foreground">
                        {results.top3[0]?.nextSteps.map((step) => (
                          <li key={step}>{step}</li>
                        ))}
                      </ol>
                    </CardContent>
                  </Card>

                  <Card className="rounded-2xl shadow-sm">
                    <CardHeader>
                      <CardTitle className="text-lg">Top score map</CardTitle>
                    </CardHeader>
                    <CardContent className="space-y-3">
                      {sortDomains(results.normalized).slice(0, 6).map(([key, value]) => (
                        <div key={key}>
                          <div className="mb-1 flex items-center justify-between text-sm">
                            <span>{DOMAIN_META[key].label}</span>
                            <span>{value}%</span>
                          </div>
                          <Progress value={value} />
                        </div>
                      ))}
                    </CardContent>
                  </Card>

                  <Card className="rounded-2xl shadow-sm">
                    <CardHeader>
                      <CardTitle className="text-lg">Start over</CardTitle>
                    </CardHeader>
                    <CardContent>
                      <Button variant="outline" onClick={resetAll} className="rounded-2xl w-full">
                        <RotateCcw className="mr-2 h-4 w-4" /> Reset assessment
                      </Button>
                    </CardContent>
                  </Card>
                </div>
              </div>
            </motion.div>
          )}
        </AnimatePresence>

        <Card className="rounded-2xl shadow-sm">
          <CardHeader>
            <CardTitle className="text-lg">Developer notes for your next upgrade</CardTitle>
          </CardHeader>
          <CardContent className="grid gap-4 md:grid-cols-2 text-sm text-muted-foreground">
            <div className="rounded-2xl border p-4">
              <p className="font-medium text-foreground mb-2">Current version includes</p>
              <ul className="list-disc pl-5 space-y-1">
                <li>Adaptive branching by cluster</li>
                <li>Weighted domain scoring</li>
                <li>Top 3 stream recommendations</li>
                <li>Anonymous analytics in localStorage</li>
              </ul>
            </div>
            <div className="rounded-2xl border p-4">
              <p className="font-medium text-foreground mb-2">Recommended future upgrade</p>
              <ul className="list-disc pl-5 space-y-1">
                <li>Connect Firebase or Supabase to collect school-wide anonymous usage stats</li>
                <li>Add admin dashboard for stream distribution and clarity improvement</li>
                <li>Add contradiction detection questions for stronger reliability</li>
                <li>Add country-specific university suggestions later</li>
              </ul>
            </div>
          </CardContent>
        </Card>
      </div>
    </div>
  );
}
