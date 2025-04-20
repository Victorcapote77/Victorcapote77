import React from "react"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { Input } from "@/components/ui/input";

export default function VictorLandingPage() { return ( <div className="bg-black text-white font-sans min-h-screen"> {/* Header */} <header className="flex flex-col md:flex-row justify-between items-center px-6 py-4 border-b border-gray-800 text-center md:text-left"> <h1 className="text-2xl font-bold mb-2 md:mb-0">VICTOR</h1> <nav className="space-x-4"> <a href="#" className="hover:text-red-500">Inicio</a> <a href="#" className="hover:text-red-500">Gorras</a> <a href="#" className="hover:text-red-500">Sobre Nosotros</a> <a href="#" className="hover:text-red-500">Contacto</a> </nav> </header>

{/* Hero Section */}
  <section className="text-center py-16 px-4">
    <img src="/logo-victor.png" alt="Victor Logo" className="mx-auto w-32 md:w-40 mb-6" />
    <h2 className="text-3xl md:text-4xl font-bold mb-4">Luce la diferencia. Viste VICTOR.</h2>
    <Button className="bg-red-600 text-white px-6 py-2 text-lg rounded-xl hover:bg-red-700">Compra ahora</Button>
  </section>

  {/* Products Section */}
  <section className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 px-4 md:px-6 py-12">
    {[1, 2, 3].map((i) => (
      <Card key={i} className="bg-zinc-900 rounded-2xl shadow-lg">
        <CardContent className="p-4">
          <img src={`/cap-${i}.png`} alt={`Gorra ${i}`} className="rounded-xl mb-4" />
          <h3 className="text-xl font-semibold mb-2">Gorra VICTOR {i}</h3>
          <p className="mb-4 text-gray-400">Diseño exclusivo con estilo moderno y urbano.</p>
          <Button className="bg-red-600 hover:bg-red-700 w-full">Agregar al carrito</Button>
        </CardContent>
      </Card>
    ))}
  </section>

  {/* Features */}
  <section className="text-center px-4 md:px-6 py-12 bg-zinc-800">
    <h3 className="text-2xl font-bold mb-6">¿Por qué elegir VICTOR?</h3>
    <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
      <div>
        <h4 className="text-lg font-semibold mb-2">Calidad Premium</h4>
        <p>Materiales duraderos y cómodos.</p>
      </div>
      <div>
        <h4 className="text-lg font-semibold mb-2">Diseños Únicos</h4>
        <p>Estilo moderno con personalidad.</p>
      </div>
      <div>
        <h4 className="text-lg font-semibold mb-2">Envíos Rápidos</h4>
        <p>Llega a tu puerta en pocos días.</p>
      </div>
    </div>
  </section>

  {/* Contact Section */}
  <section className="px-4 md:px-6 py-12 text-center">
    <h3 className="text-2xl font-bold mb-4">Suscríbete para recibir novedades</h3>
    <div className="flex flex-col sm:flex-row justify-center gap-4 max-w-md mx-auto">
      <Input placeholder="Tu correo electrónico" className="text-black w-full" />
      <Button className="bg-red-600 hover:bg-red-700 w-full sm:w-auto">Suscribirme</Button>
    </div>
  </section>

  {/* Footer */}
  <footer className="px-6 py-4 text-center text-gray-400 border-t border-gray-800">
    © {new Date().getFullYear()} VICTOR. Todos los derechos reservados.
  </footer>
</div>

); }

