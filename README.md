import * as React from "react"
import { Button } from "@/components/ui/button"
import { Card, CardContent, CardDescription, CardHeader, CardTitle, CardFooter } from "@/components/ui/card"
import { Input } from "@/components/ui/input"
import { BrainCircuit, HeartPulse, Users, Clock, DollarSign, BarChart, MessageCircle } from "lucide-react"
import Link from 'next/link'

export default function AnoiaLandingPage() {
  return (
    <div className="flex flex-col min-h-screen bg-cyan-50">
      <header className="px-4 lg:px-6 h-14 flex items-center bg-cyan-600 text-white">
        <Link className="flex items-center justify-center" href="#">
          <BrainCircuit className="h-6 w-6" />
          <span className="ml-2 font-bold">Anoia</span>
        </Link>
        <nav className="ml-auto flex gap-4 sm:gap-6">
          <Link className="text-sm font-medium hover:underline underline-offset-4" href="#features">
            Features
          </Link>
          <Link className="text-sm font-medium hover:underline underline-offset-4" href="#about">
            About
          </Link>
          <Link className="text-sm font-medium hover:underline underline-offset-4" href="#impact">
            Impact
          </Link>
          <Link className="text-sm font-medium hover:underline underline-offset-4" href="#contact">
            Contact
          </Link>
        </nav>
      </header>
      <main className="flex-1">
        {/* Hero Section */}
        <section className="w-full py-12 md:py-24 lg:py-32 xl:py-48">
          <div className="container px-4 md:px-6">
            <div className="flex flex-col items-center space-y-4 text-center">
              <div className="space-y-2">
                <h1 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl lg:text-6xl/none text-cyan-800">
                  Anoia: Transforming Dementia Care with AI
                </h1>
                <p className="mx-auto max-w-[700px] text-cyan-600 md:text-xl">
                  Affordable diagnosis, personalized treatment, and 24/7 caregiver support powered by AI
                </p>
              </div>
              <div className="space-x-4">
                <Button className="bg-cyan-600 hover:bg-cyan-700">Get Started</Button>
                <Button variant="outline" className="text-cyan-600 border-cyan-600 hover:bg-cyan-100">Learn More</Button>
              </div>
            </div>
          </div>
        </section>

        {/* About Section */}
        <section id="about" className="w-full py-12 md:py-24 lg:py-32 bg-white">
          <div className="container px-4 md:px-6">
            <h2 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-center mb-8 text-cyan-800">About Anoia</h2>
            <p className="mx-auto max-w-[800px] text-cyan-600 md:text-xl text-center">
              Anoia is an innovative AI-powered platform designed to revolutionize dementia care. Developed by a multi-disciplinary team of experts from Harvard and MIT, including neurologists, data scientists, and healthcare professionals, Anoia harnesses cutting-edge artificial intelligence and machine learning algorithms to provide a holistic and efficient approach to dementia management.
            </p>
          </div>
        </section>

        {/* Features Section */}
        <section id="features" className="w-full py-12 md:py-24 lg:py-32 bg-cyan-50">
          <div className="container px-4 md:px-6">
            <h2 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-center mb-8 text-cyan-800">Key Features</h2>
            <div className="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <BrainCircuit className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Early Detection and Diagnosis</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Advanced speech analysis and cognitive assessment tools to detect subtle signs of cognitive decline, enabling early diagnosis of various forms of dementia.</p>
                </CardContent>
              </Card>
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <HeartPulse className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Personalized Treatment Planning</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Tailored treatment recommendations and care plans based on integrated patient data from multiple sources, optimizing interventions and resource utilization.</p>
                </CardContent>
              </Card>
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <Users className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Comprehensive Caregiver Support</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Educational materials, stress management techniques, medication reminders, community support forums, and AI-powered assistance for 24/7 support.</p>
                </CardContent>
              </Card>
            </div>
          </div>
        </section>

        {/* Ana Chatbot Section */}
        <section id="ana-chatbot" className="w-full py-12 md:py-24 lg:py-32 bg-white">
          <div className="container px-4 md:px-6">
            <h2 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-center mb-8 text-cyan-800">Meet Ana: Your AI Caregiver Assistant</h2>
            <p className="mx-auto max-w-[700px] text-cyan-600 md:text-xl text-center mb-8">
              Ana is our intelligent chatbot, designed specifically to support family caregivers of people with dementia. Available 24/7, Ana provides instant answers, emotional support, and personalized advice to help you navigate the challenges of caregiving.
            </p>
            <div className="flex justify-center">
              <button
                onClick={() => {
                  window.open(
                    'https://www.stack-ai.com/chat-assistant/22327fa5-e742-4088-aff9-af1528b0a39e/78489e95-89c5-4910-974b-6b4f0aa7fc2e/66fdc8f95845c9fce44605d1',
                    'AnaChatbot',
                    'width=400,height=600,resizable=yes,scrollbars=yes'
                  );
                }}
                className="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md text-white bg-cyan-600 hover:bg-cyan-700 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-cyan-500"
              >
                <MessageCircle className="w-5 h-5 mr-2" />
                Ask Ana
              </button>
            </div>
          </div>
        </section>

        {/* Impact Section */}
        <section id="impact" className="w-full py-12 md:py-24 lg:py-32 bg-cyan-50">
          <div className="container px-4 md:px-6">
            <h2 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-center mb-8 text-cyan-800">Impact and Potential</h2>
            <div className="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <Clock className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Early Intervention</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Timely detection and intervention lead to better health outcomes and improved quality of life for patients.</p>
                </CardContent>
              </Card>
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <DollarSign className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Cost-Effectiveness</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Reduces long-term costs associated with advanced-stage dementia care through early diagnosis and personalized treatment plans.</p>
                </CardContent>
              </Card>
              <Card className="bg-white border-cyan-200">
                <CardHeader>
                  <BarChart className="h-6 w-6 mb-2 text-cyan-600" />
                  <CardTitle className="text-cyan-800">Scalable Solution</CardTitle>
                </CardHeader>
                <CardContent>
                  <p className="text-cyan-600">Addresses the growing global challenge of dementia with a scalable and accessible approach, promoting a more sustainable healthcare model.</p>
                </CardContent>
              </Card>
            </div>
          </div>
        </section>

        {/* Contact Section */}
        <section id="contact" className="w-full py-12 md:py-24 lg:py-32 bg-white">
          <div className="container px-4 md:px-6">
            <h2 className="text-3xl font-bold tracking-tighter sm:text-4xl md:text-5xl text-center mb-8 text-cyan-800">Contact Us</h2>
            <div className="mx-auto max-w-[500px]">
              <Card className="bg-cyan-50 border-cyan-200">
                <CardHeader>
                  <CardTitle className="text-cyan-800">Get in touch</CardTitle>
                  <CardDescription className="text-cyan-600">We're here to help with any questions about Anoia.</CardDescription>
                </CardHeader>
                <CardContent>
                  <form>
                    <div className="grid w-full items-center gap-4">
                      <div className="flex flex-col space-y-1.5">
                        <Input id="name" placeholder="Name" className="border-cyan-300 focus:border-cyan-500" />
                      </div>
                      <div className="flex flex-col space-y-1.5">
                        <Input id="email" placeholder="Email" type="email" className="border-cyan-300 focus:border-cyan-500" />
                      </div>
                      <div className="flex flex-col space-y-1.5">
                        <Input id="message" placeholder="Your message" className="border-cyan-300 focus:border-cyan-500" />
                      </div>
                    </div>
                  </form>
                </CardContent>
                <CardFooter className="flex justify-between">
                  <Button className="w-full bg-cyan-600 hover:bg-cyan-700">Send Message</Button>
                </CardFooter>
              </Card>
            </div>
          </div>
        </section>
      </main>
      <footer className="flex flex-col gap-2 sm:flex-row py-6 w-full shrink-0 items-center px-4 md:px-6 border-t border-cyan-200 bg-cyan-50">
        <p className="text-xs text-cyan-600">© 2024 Anoia. All rights reserved.</p>
        <nav className="sm:ml-auto flex gap-4 sm:gap-6">
          <Link className="text-xs hover:underline underline-offset-4 text-cyan-600" href="#">
            Terms of Service
          </Link>
          <Link className="text-xs hover:underline underline-offset-4 text-cyan-600" href="#">
            Privacy
          </Link>
        </nav>
      </footer>
    </div>
  )
}
