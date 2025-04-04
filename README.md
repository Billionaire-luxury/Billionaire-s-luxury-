# Billionaire-s-luxury-
import React from "react"; import { Input } from "@/components/ui/input"; import { Button } from "@/components/ui/button"; import { Card, CardContent } from "@/components/ui/card"; import { ShoppingCart, Search } from "lucide-react";

export default function Home() { return ( <div className="min-h-screen bg-white text-black"> {/* Header */} <header className="flex justify-between items-center p-4 shadow-md"> <h1 className="text-2xl font-bold">Billionaire's Luxury</h1> <div className="flex gap-2 items-center"> <Input placeholder="Search for products..." className="w-64" /> <Button variant="outline"> <Search className="w-4 h-4" /> </Button> <Button variant="outline"> <ShoppingCart className="w-5 h-5" /> </Button> </div> </header>

{/* Filters */}
  <div className="grid grid-cols-1 md:grid-cols-4 gap-4 p-4">
    <div className="space-y-4">
      <div>
        <h2 className="font-semibold">Filter by Size</h2>
        <select className="w-full p-2 border rounded">
          <option>All</option>
          <option>Small</option>
          <option>Medium</option>
          <option>Large</option>
        </select>
      </div>
      <div>
        <h2 className="font-semibold">Filter by Color</h2>
        <select className="w-full p-2 border rounded">
          <option>All</option>
          <option>Black</option>
          <option>White</option>
          <option>Red</option>
          <option>Blue</option>
        </select>
      </div>
      <div>
        <h2 className="font-semibold">Filter by Price</h2>
        <select className="w-full p-2 border rounded">
          <option>All</option>
          <option>Under $50</option>
          <option>$50 - $100</option>
          <option>Over $100</option>
        </select>
      </div>
      <div>
        <h2 className="font-semibold">Sort by</h2>
        <select className="w-full p-2 border rounded">
          <option>Relevance</option>
          <option>Price: Low to High</option>
          <option>Price: High to Low</option>
        </select>
      </div>
    </div>

    {/* Products */}
    <div className="md:col-span-3 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
      {[1, 2, 3, 4, 5, 6].map((id) => (
        <Card key={id} className="hover:shadow-xl transition-shadow">
          <CardContent className="p-4">
            <div className="h-40 bg-gray-100 rounded mb-2" />
            <h3 className="font-semibold">Product Name</h3>
            <p className="text-sm text-gray-500">$99.99</p>
            <Button className="mt-2 w-full">Add to Cart</Button>
          </CardContent>
        </Card>
      ))}
    </div>
  </div>
</div>

); }
google09265806da70a18b.html
