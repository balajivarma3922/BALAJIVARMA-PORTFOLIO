import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Github, Linkedin, Mail, Phone } from "lucide-react";

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 via-purple-50 to-pink-50 text-gray-900">
      {/* Header */}
      <header className="p-6 shadow-lg bg-white/70 backdrop-blur-md sticky top-0 z-50 rounded-b-2xl">
        <div className="max-w-6xl mx-auto flex justify-between items-center">
          <h1 className="text-2xl font-extrabold text-blue-700">Bathula Balaji Varma</h1>
          <nav className="space-x-6 font-medium">
            <a href="#about" className="hover:text-purple-600 transition">About</a>
            <a href="#skills" className="hover:text-purple-600 transition">Skills</a>
            <a href="#projects" className="hover:text-purple-600 transition">Projects</a>
            <a href="#contact" className="hover:text-purple-600 transition">Contact</a>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section className="flex flex-col items-center justify-center text-center py-28 bg-gradient-to-r from-blue-100 via-purple-100 to-pink-100">
        <motion.h2 initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} className="text-5xl font-extrabold mb-6 text-purple-700">
          Hi, I’m Bathula Balaji Varma 👋
        </motion.h2>
        <p className="text-lg max-w-2xl text-gray-700 leading-relaxed">
          Passionate about building intelligent systems and enhancing digital security. Eager to contribute technical expertise and problem-solving skills in a dynamic tech-driven environment.
        </p>
        <div className="mt-8 space-x-4">
          <Button className="rounded-full bg-purple-600 hover:bg-purple-700 text-white shadow-lg px-6 py-2">View Resume</Button>
          <Button variant="outline" className="rounded-full border-purple-600 text-purple-600 hover:bg-purple-50 shadow px-6 py-2">Contact Me</Button>
        </div>
      </section>

      {/* About Section */}
      <section id="about" className="max-w-6xl mx-auto py-20 px-6">
        <h3 className="text-4xl font-bold mb-8 text-center text-purple-700">About Me</h3>
        <div className="bg-white/80 shadow-lg rounded-2xl p-8 leading-relaxed">
          <p>
            Machine learning internship at BIST Technology (2023), where I worked on developing predictive models and analyzing datasets for intelligent decision-making. Skilled in Python, data preprocessing, and ML algorithms. Strong foundation in AI concepts with practical exposure to model development and evaluation. Eager to contribute to innovative projects in AI, ML, or data science domains.
          </p>
          <p className="mt-4">
            TEGA (Sand Space Technologies, 2025), exploring digital security frameworks and ethical practices. Proficient in Python, data analysis, ML algorithms, and cybersecurity tools. Highly motivated to contribute to innovative AI or cybersecurity-driven environments with a commitment to continuous learning and growth.
          </p>
          <h4 className="text-2xl font-semibold mt-8">Academic History</h4>
          <ul className="list-disc ml-6 mt-2 text-gray-700">
            <li>Chaitanya Bharathi Innovative School (2019–2020) – GPA 10.0</li>
            <li>Sri Chaitanya College (2020–2022) – 80%</li>
            <li>B.Sc. in Computer Engineering (Artificial Intelligence), MVR College of Engineering and Technology (2022–2026) – GPA: 8.4 (upto 4-1)</li>
          </ul>
          <h4 className="text-2xl font-semibold mt-8">Certifications</h4>
          <ul className="list-disc ml-6 mt-2 text-gray-700">
            <li>Machine Learning – BIST Technologies (2023)</li>
            <li>Cyber Security Moderation – HP Life (2024)</li>
            <li>Cyber Security – TEGA (Sand Space Technologies, 2025)</li>
          </ul>
        </div>
      </section>

      {/* Skills Section */}
      <section id="skills" className="bg-gradient-to-r from-purple-50 to-pink-50 py-20 px-6">
        <h3 className="text-4xl font-bold mb-10 text-center text-purple-700">Skills</h3>
        <div className="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-6 gap-6 text-center max-w-5xl mx-auto">
          {['Python','Java','Machine Learning','Deep Learning','Data Preprocessing','Cybersecurity'].map(skill => (
            <div key={skill} className="p-4 bg-white rounded-2xl shadow-lg hover:shadow-xl transition text-purple-700 font-semibold">
              {skill}
            </div>
          ))}
        </div>
      </section>

      {/* Projects Section */}
      <section id="projects" className="bg-gray-100 py-20 px-6">
        <div className="max-w-6xl mx-auto">
          <h3 className="text-4xl font-bold mb-10 text-center text-purple-700">Projects & Internships</h3>
          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
            <Card className="rounded-2xl shadow-lg hover:shadow-2xl transition bg-white/90">
              <CardContent className="p-6">
                <h4 className="text-2xl font-semibold text-purple-700">Machine Learning Internship</h4>
                <p className="text-gray-600 mt-2">BIST Technology (2023) – Developed predictive models and performed data preprocessing for intelligent decision-making.</p>
                <div className="mt-4 flex space-x-3">
                  <Button size="sm" className="bg-purple-600 text-white hover:bg-purple-700 rounded-full">Details</Button>
                </div>
              </CardContent>
            </Card>
            <Card className="rounded-2xl shadow-lg hover:shadow-2xl transition bg-white/90">
              <CardContent className="p-6">
                <h4 className="text-2xl font-semibold text-purple-700">Cybersecurity Internship</h4>
                <p className="text-gray-600 mt-2">TEGA (Sand Space Technologies, 2025) – Explored digital security frameworks and ethical practices using Python and cybersecurity tools.</p>
                <div className="mt-4 flex space-x-3">
                  <Button size="sm" className="bg-purple-600 text-white hover:bg-purple-700 rounded-full">Details</Button>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Contact Section */}
      <section id="contact" className="bg-gradient-to-r from-pink-50 via-purple-50 to-blue-50 py-20 px-6 text-center">
        <h3 className="text-4xl font-bold mb-6 text-purple-700">Get in Touch</h3>
        <p className="text-gray-700 mb-8">Feel free to reach out via email, phone, or connect on social platforms.</p>
        <div className="flex justify-center space-x-6">
          <a href="mailto:bpadma024@gmail.com" className="p-4 bg-white rounded-full shadow-lg hover:shadow-2xl transition text-purple-700">
            <Mail />
          </a>
          <a href="tel:9346564787" className="p-4 bg-white rounded-full shadow-lg hover:shadow-2xl transition text-purple-700">
            <Phone />
          </a>
          <a href="https://github.com/" target="_blank" className="p-4 bg-white rounded-full shadow-lg hover:shadow-2xl transition text-purple-700">
            <Github />
          </a>
          <a href="https://linkedin.com/" target="_blank" className="p-4 bg-white rounded-full shadow-lg hover:shadow-2xl transition text-purple-700">
            <Linkedin />
          </a>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-6 bg-white/80 text-center border-t">
        <p className="text-sm text-gray-600">© {new Date().getFullYear()} Bathula Balaji Varma. All rights reserved.</p>
      </footer>
    </div>
  );
}
