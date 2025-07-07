# Minha-loja-de-licen-as-
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Loja de Chaves Windows</title>
  <style>
    body { font-family: Arial; margin: 0; padding: 0; background: #f4f4f4; }
    header, footer { background: #111; color: white; padding: 1rem; text-align: center; }
    .container { padding: 2rem; max-width: 800px; margin: auto; }
    .product { background: white; padding: 1rem; margin-bottom: 1rem; border-radius: 8px; box-shadow: 0 0 8px rgba(0,0,0,0.1); }
    .btn { background: green; color: white; padding: 0.5rem 1rem; border: none; cursor: pointer; }
  </style>
</head>
<body>
  <header>
    <h1>Chaves de Windows Originais</h1>
  </header>

  <div class="container">
    <div class="product">
      <h2>Windows 10 Pro - Licença Digital</h2>
      <p>Ativação permanente. Envio imediato por e-mail.</p>
      <p><strong>R$ 69,90</strong></p>
      <button class="btn">Comprar</button>
    </div>
    <div class="product">
      <h2>Windows 11 Pro - Licença Digital</h2>
      <p>Compatível com PCs modernos. Envio imediato.</p>
      <p><strong>R$ 79,90</strong></p>
      <button class="btn">Comprar</button>
    </div>
  </div>

  <footer>
    <p>&copy; 2025 Minha Loja de Licenças</p>
  </footer>
</body>
</html>
import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { ShoppingCart, Mail } from "lucide-react";

const products = [
  {
    id: 1,
    name: "Windows 10 Pro",
    description: "Licença digital, ativação imediata.",
    price: 5.0,
  },
  {
    id: 2,
    name: "Windows 11 Pro",
    description: "Licença digital, compatível com PCs modernos.",
    price: 79.9,
  },
];

export default function Store() {
  return (
    <div className="min-h-screen bg-gray-100 p-6">
      <header className="bg-black text-white p-4 rounded-2xl shadow-md mb-6">
        <h1 className="text-2xl font-bold">Minha Loja de Chaves Windows</h1>
      </header>

      <div className="grid gap-4 md:grid-cols-2">
        {products.map((product) => (
          <Card key={product.id} className="rounded-2xl shadow">
            <CardContent className="p-4 space-y-2">
              <h2 className="text-xl font-semibold">{product.name}</h2>
              <p className="text-gray-600">{product.description}</p>
              <p className="text-green-700 font-bold">R$ {product.price.toFixed(2)}</p>
              <Button className="w-full flex gap-2">
                <ShoppingCart size={18} /> Comprar
              </Button>
            </CardContent>
          </Card>
        ))}
      </div>

      <footer className="mt-10 text-center text-gray-500 text-sm">
        <p>&copy; 2025 Minha Loja Digital - Todos os direitos reservados.</p>
      </footer>
    </div>
  );
}
