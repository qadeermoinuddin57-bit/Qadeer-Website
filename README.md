# Qadeer-Website
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";
import { Github, Linkedin, Mail, Home, Code, Briefcase, FolderGit2 } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-gray-900 via-gray-800 to-gray-700 text-white font-sans scroll-smooth">
      {/* Navigation */}
      <nav className="fixed top-0 left-0 w-full bg-gray-900 bg-opacity-90 backdrop-blur-md border-b border-gray-800 z-50">
        <div className="max-w-6xl mx-auto px-6 py-4 flex justify-between items-center">
          <h1 className="text-xl font-semibold text-blue-400">Qadeer Mohammed</h1>
          <div className="flex gap-6 text-gray-300 text-sm">
            <a href="#home" className="hover:text-blue-400 flex items-center gap-1"><Home className="w-4 h-4"/>Home</a>
            <a href="#skills" className="hover:text-blue-400 flex items-center gap-1"><Code className="w-4 h-4"/>Skills</a>
            <a href="#experience" className="hover:text-blue-400 flex items-center gap-1"><Briefcase className="w-4 h-4"/>Experience</a>
            <a href="#projects" className="hover:text-blue-400 flex items-center gap-1"><FolderGit2 className="w-4 h-4"/>Projects</a>
            <a href="#contact" className="hover:text-blue-400">Contact</a>
          </div>
        </div>
      </nav>

      {/* Header */}
      <header id="home" className="text-center py-32 md:py-40">
        <motion.h1 
          initial={{ opacity: 0, y: -20 }} 
          animate={{ opacity: 1, y: 0 }} 
          className="text-5xl font-bold mb-4 text-blue-400">
          Qadeer Mohammed
        </motion.h1>
        <p className="text-xl text-gray-300 max-w-3xl mx-auto">
          Data Scientist | AI & ML Specialist | Data Engineer
        </p>
        <div className="flex justify-center gap-6 mt-6">
          <a href="mailto:qadeermoinuddin57@gmail.com"><Mail className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
          <a href="https://linkedin.com/in/moinuddin57" target="_blank"><Linkedin className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
          <a href="https://github.com/moinuddin57" target="_blank"><Github className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
        </div>
        <div className="mt-8">
          <Button variant="secondary" asChild>
            <a href="/resume.pdf" download>Download Resume</a>
          </Button>
        </div>
      </header>

      {/* Summary */}
      <section className="max-w-5xl mx-auto px-6 mb-20" id="about">
        <Card className="bg-gray-800 border border-gray-700 rounded-2xl shadow-lg">
          <CardContent className="p-8 text-gray-200 leading-relaxed">
            Data Scientist with 5+ years of experience in advanced analytics and AI/ML expertise, specializing in building intelligent systems that deliver financial savings and drive margin expansion. Proven ability to design and implement AI Agents and models to improve decision-making and operational efficiency. Proficient in Python, Scikit-learn, Pandas, and SQL, with strong exposure to GenAI and Agentic AI workflows.
          </CardContent>
        </Card>
      </section>

      {/* Skills Section */}
      <section className="max-w-6xl mx-auto px-6 mb-20" id="skills">
        <h2 className="text-3xl font-semibold mb-10 text-center text-blue-400">Technical Skills</h2>
        <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6">
          {["Python", "SQL", "Scikit-learn", "Pandas", "Power BI", "Looker", "Tableau", "Databricks", "Apache Spark", "Airflow", "GenAI", "Agentic AI", "ETL/ELT", "Data Cleaning"].map((skill, idx) => (
            <motion.div key={idx} whileHover={{ scale: 1.05 }} className="bg-gray-800 border border-gray-700 text-center py-4 rounded-xl shadow-md">
              {skill}
            </motion.div>
          ))}
        </div>
      </section>

      {/* Experience Section */}
      <section className="max-w-6xl mx-auto px-6 mb-20" id="experience">
        <h2 className="text-3xl font-semibold mb-10 text-center text-blue-400">Experience</h2>
        <div className="grid md:grid-cols-2 gap-8">
          <Card className="bg-gray-800 border border-gray-700">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Data Scientist - Netmeds</h3>
              <p className="text-gray-400 mb-4">Aug 2022 - June 2023</p>
              <ul className="list-disc ml-5 text-gray-300 space-y-2">
                <li>Applied AI/ML techniques to identify process inefficiencies and drive operational margin expansion.</li>
                <li>Built scalable pipelines with Python, Spark, and cloud services, ensuring 99.8% uptime.</li>
                <li>Developed Python APIs for ETL automation, saving 45+ hours per month.</li>
                <li>Reduced recurring incidents by 30% through root-cause analysis and preventive measures.</li>
              </ul>
            </CardContent>
          </Card>

          <Card className="bg-gray-800 border border-gray-700">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Data Scientist Intern - CRED</h3>
              <p className="text-gray-400 mb-4">June 2019 - Aug 2022</p>
              <ul className="list-disc ml-5 text-gray-300 space-y-2">
                <li>Built optimized real-time data pipelines using SQL and GCP BigQuery.</li>
                <li>Developed self-serve decision dashboards with Power BI and Looker.</li>
                <li>Enhanced fraud detection models using clustering, regression, and outlier analysis.</li>
                <li>Automated data integrity checks to ensure 99%+ accuracy in downstream models.</li>
              </ul>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Projects Section */}
      <section className="max-w-6xl mx-auto px-6 mb-20" id="projects">
        <h2 className="text-3xl font-semibold mb-10 text-center text-blue-400">Projects</h2>
        <div className="grid md:grid-cols-2 gap-8">
          <Card className="bg-gray-800 border border-gray-700">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Low-Code AI Pipeline for Retail Forecasting</h3>
              <p className="text-gray-300 mb-4">Designed an AI workflow integrated with Power BI for demand forecasting, improving product inventory accuracy and analytics visualization.</p>
              <Button variant="secondary" asChild>
                <a href="https://some-link.com" target="_blank">View Demo</a>
              </Button>
            </CardContent>
          </Card>

          <Card className="bg-gray-800 border border-gray-700">
            <CardContent className="p-6">
              <h3 className="text-xl font-semibold mb-2">Tech Industry Salary Distribution Analysis</h3>
              <p className="text-gray-300 mb-4">Analyzed salary distribution across tech roles using Python, SQL, and Power BI to uncover trends and career insights.</p>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* Education */}
      <section className="max-w-4xl mx-auto px-6 mb-20 text-center" id="education">
        <h2 className="text-3xl font-semibold mb-6 text-blue-400">Education</h2>
        <p className="text-xl text-gray-200">M.S. in Data Science — University of the Cumberlands (GPA: 4.0/4.0)</p>
        <p className="text-gray-400 mt-2">Expected Graduation: Dec 2024</p>
      </section>

      {/* Contact */}
      <section id="contact" className="max-w-4xl mx-auto text-center px-6 pb-20">
        <h2 className="text-3xl font-semibold mb-6 text-blue-400">Get in Touch</h2>
        <p className="text-gray-300 mb-4">Feel free to reach out for collaboration, opportunities, or networking.</p>
        <div className="flex justify-center gap-6">
          <a href="mailto:qadeermoinuddin57@gmail.com"><Mail className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
          <a href="https://linkedin.com/in/moinuddin57" target="_blank"><Linkedin className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
          <a href="https://github.com/moinuddin57" target="_blank"><Github className="w-6 h-6 text-gray-300 hover:text-blue-400"/></a>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center py-8 border-t border-gray-700 text-gray-400">
        © {new Date().getFullYear()} Qadeer Mohammed. All rights reserved.
      </footer>
    </div>
  );
}
