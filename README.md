 # SOHAN
import React from 'react';
import { Github, Linkedin, Mail, Terminal, Cpu, Code2, ExternalLink } from 'lucide-react';

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-slate-950 text-slate-200 font-mono selection:bg-sky-500/30">
      
      {/* Navigation */}
      <nav className="fixed w-full backdrop-blur-md bg-slate-950/80 border-b border-slate-800 z-50">
        <div className="max-w-5xl mx-auto px-6 h-16 flex items-center justify-between">
          <span className="text-sky-400 font-bold text-xl">alex_dev ~/</span>
          <div className="flex gap-6 text-sm">
            <a href="#about" className="hover:text-sky-400 transition-colors">_about</a>
            <a href="#stack" className="hover:text-sky-400 transition-colors">_stack</a>
            <a href="#projects" className="hover:text-sky-400 transition-colors">_projects</a>
          </div>
        </div>
      </nav>

      <main className="max-w-5xl mx-auto px-6 pt-32 pb-20">
        
        {/* Hero Section */}
        <section id="about" className="min-h-[60vh] flex flex-col justify-center mb-24">
          <div className="flex items-start gap-4 mb-6 text-sky-400 animate-pulse">
            <Terminal size={24} />
            <span>System.out.println("Hello World");</span>
          </div>
          
          <h1 className="text-6xl font-bold text-slate-100 mb-6 tracking-tight">
            Alex Dev
          </h1>
          <h2 className="text-3xl text-slate-400 mb-8">
            Computer Engineer & <span className="text-sky-400">Systems Architect</span>
          </h2>
          <p className="text-lg text-slate-400 max-w-2xl leading-relaxed mb-10">
            I bridge the gap between hardware and software. Specialized in Embedded Systems, 
            Cloud Infrastructure, and High-Performance Computing. Currently optimizing 
            low-latency networks at TechCorp.
          </p>
          
          <div className="flex gap-4">
            <a href="https://github.com" target="_blank" rel="noreferrer" 
               className="flex items-center gap-2 px-6 py-3 bg-slate-800 hover:bg-slate-700 rounded-lg transition-all border border-slate-700 hover:border-sky-400">
              <Github size={20} />
              <span>GitHub</span>
            </a>
            <a href="https://linkedin.com" target="_blank" rel="noreferrer"
               className="flex items-center gap-2 px-6 py-3 bg-slate-800 hover:bg-slate-700 rounded-lg transition-all border border-slate-700 hover:border-sky-400">
              <Linkedin size={20} />
              <span>LinkedIn</span>
            </a>
          </div>
        </section>

        {/* Tech Stack Section */}
        <section id="stack" className="mb-32">
          <div className="flex items-center gap-3 mb-12">
            <Cpu className="text-sky-400" />
            <h2 className="text-2xl font-bold">Technical Arsenal</h2>
          </div>

          <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
            {/* Category 1 */}
            <div className="bg-slate-900/50 p-6 rounded-xl border border-slate-800 hover:border-slate-600 transition-all">
              <h3 className="text-sky-400 font-bold mb-4 flex items-center gap-2">
                <Code2 size={18} /> Languages
              </h3>
              <ul className="space-y-2 text-slate-400">
                <li>C / C++ (Modern)</li>
                <li>Python / Rust</li>
                <li>TypeScript</li>
                <li>Verilog / VHDL</li>
              </ul>
            </div>

            {/* Category 2 */}
            <div className="bg-slate-900/50 p-6 rounded-xl border border-slate-800 hover:border-slate-600 transition-all">
              <h3 className="text-sky-400 font-bold mb-4 flex items-center gap-2">
                <Cpu size={18} /> Embedded & IoT
              </h3>
              <ul className="space-y-2 text-slate-400">
                <li>RTOS (FreeRTOS)</li>
                <li>Raspberry Pi / Arduino</li>
                <li>I2C / SPI / UART</li>
                <li>PCB Design (KiCad)</li>
              </ul>
            </div>

            {/* Category 3 */}
            <div className="bg-slate-900/50 p-6 rounded-xl border border-slate-800 hover:border-slate-600 transition-all">
              <h3 className="text-sky-400 font-bold mb-4 flex items-center gap-2">
                <Terminal size={18} /> DevOps & Tools
              </h3>
              <ul className="space-y-2 text-slate-400">
                <li>Docker / Kubernetes</li>
                <li>AWS (EC2, Lambda)</li>
                <li>Linux Kernel Modules</li>
                <li>CI/CD Pipelines</li>
              </ul>
            </div>
          </div>
        </section>

        {/* Projects Section */}
        <section id="projects" className="mb-32">
          <div className="flex items-center gap-3 mb-12">
            <Code2 className="text-sky-400" />
            <h2 className="text-2xl font-bold">Engineered Systems</h2>
          </div>

          <div className="space-y-12">
            {/* Project 1 */}
            <div className="group relative bg-slate-900 rounded-2xl border border-slate-800 p-8 hover:border-sky-500/50 transition-all">
              <div className="absolute top-0 right-0 p-6 opacity-0 group-hover:opacity-100 transition-opacity">
                <ExternalLink className="text-sky-400" />
              </div>
              
              <div className="flex flex-col md:flex-row gap-8">
                <div className="md:w-2/3">
                  <h3 className="text-2xl font-bold text-slate-100 mb-4 group-hover:text-sky-400 transition-colors">
                    Autonomous Drone Navigation System
                  </h3>
                  <p className="text-slate-400 mb-6 leading-relaxed">
                    Developed a custom flight controller using an STM32 microcontroller. 
                    Implemented PID control algorithms and sensor fusion (Kalman Filter) 
                    for stable flight in GPS-denied environments.
                  </p>
                  <div className="flex flex-wrap gap-3">
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">C++</span>
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">STM32</span>
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">Kalman Filters</span>
                  </div>
                </div>
              </div>
            </div>

            {/* Project 2 */}
            <div className="group relative bg-slate-900 rounded-2xl border border-slate-800 p-8 hover:border-sky-500/50 transition-all">
              <div className="absolute top-0 right-0 p-6 opacity-0 group-hover:opacity-100 transition-opacity">
                <ExternalLink className="text-sky-400" />
              </div>
              
              <div className="flex flex-col md:flex-row gap-8">
                <div className="md:w-2/3">
                  <h3 className="text-2xl font-bold text-slate-100 mb-4 group-hover:text-sky-400 transition-colors">
                    Distributed File System
                  </h3>
                  <p className="text-slate-400 mb-6 leading-relaxed">
                    Designed a fault-tolerant distributed file system inspired by GFS. 
                    Features include chunk replication, master-worker architecture, 
                    and automatic failure recovery.
                  </p>
                  <div className="flex flex-wrap gap-3">
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">Go</span>
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">gRPC</span>
                    <span className="px-3 py-1 bg-slate-800 rounded-full text-xs text-sky-300 border border-slate-700">Distributed Systems</span>
                  </div>
                </div>
              </div>
            </div>

          </div>
        </section>

        {/* Contact / Footer */}
        <section className="text-center border-t border-slate-800 pt-20">
          <h2 className="text-3xl font-bold text-slate-100 mb-6">Ready to collaborate?</h2>
          <p className="text-slate-400 mb-8">
            I am currently open to roles in Embedded Engineering and Backend Development.
          </p>
          <a href="mailto:hello@example.com" className="inline-flex items-center gap-2 px-8 py-4 bg-sky-600 hover:bg-sky-500 text-white rounded-lg font-bold transition-all">
            <Mail size={20} />
            Initialize Handshake
          </a>
        </section>

      </main>
    </div>
  );
}
