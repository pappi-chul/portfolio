# portfolio
Portfolio
import { useState } from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { FaGithub, FaLinkedin, FaEnvelope } from "react-icons/fa";

export default function Portfolio() {
  const [darkMode, setDarkMode] = useState(false);

  return (
    <div className={`min-h-screen ${darkMode ? "bg-gray-900 text-white" : "bg-white text-black"}`}>
      <header className="p-6 flex justify-between items-center">
        <h1 className="text-3xl font-bold">Jeremiah Irenaye</h1>
        <button onClick={() => setDarkMode(!darkMode)} className="p-2 border rounded-lg">
          {darkMode ? "Light Mode" : "Dark Mode"}
        </button>
      </header>

      <section className="text-center py-16">
        <motion.h2 initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} className="text-5xl font-bold">
          Hi, I'm Jeremiah Irenaye
        </motion.h2>
        <p className="mt-4 text-lg">Hello! My name is Jeremiah. I am a passionate community manager/moderator and software developer with experience in building web applications using modern technologies. I enjoy solving complex problems and continuously learning new skills to improve my craft.</p>
      </section>

      <section className="py-16 px-6 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <motion.div initial={{ opacity: 0, scale: 0.9 }} animate={{ opacity: 1, scale: 1 }}>
          <Card>
            <CardContent className="p-4">
              <h3 className="text-xl font-bold">DW Tech</h3>
              <p className="mt-2">A computer store website showcasing various tech products.</p>
              <a href="https://grace-kid.github.io/D.W.T-computer-store/" target="_blank" rel="noopener noreferrer">
                <Button className="mt-4">View Project</Button>
              </a>
            </CardContent>
          </Card>
        </motion.div>
        <motion.div initial={{ opacity: 0, scale: 0.9 }} animate={{ opacity: 1, scale: 1 }}>
          <Card>
            <CardContent className="p-4">
              <h3 className="text-xl font-bold">GP Calculator</h3>
              <p className="mt-2">A GPA calculator for ESUT students to compute their grades.</p>
              <a href="https://grace-kid.github.io/ESUT-GP-Calculator/" target="_blank" rel="noopener noreferrer">
                <Button className="mt-4">View Project</Button>
              </a>
            </CardContent>
          </Card>
        </motion.div>
      </section>

      <section className="text-center py-16">
        <h2 className="text-3xl font-bold">Get in Touch</h2>
        <div className="flex justify-center gap-6 mt-4">
          <a href="https://github.com/pappi-chul" target="_blank" rel="noopener noreferrer">
            <FaGithub size={32} />
          </a>
          <a href="https://www.linkedin.com/in/jeremiah-irenaye-a81890312/" target="_blank" rel="noopener noreferrer">
            <FaLinkedin size={32} />
          </a>
          <a href="mailto:jerem2irenaye@gmail.com">
            <FaEnvelope size={32} />
          </a>
        </div>
      </section>
    </div>
  );
}
