import React, { useState } from "react";

function Dropdown() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div className="relative inline-block text-left">
      <div onClick={() => setIsOpen(!isOpen)}>
        <img
          src="https://images.pexels.com/photos/1681010/pexels-photo-1681010.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"
          alt="Usuário"
          className="w-[44px] border border-gray-300 rounded-full aspect-square object-cover "
        />
      </div>
      {isOpen && (
        <div className="absolute right-0 z-10 mt-2 w-56 origin-top-right rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none">
          <div>
            <a
              href="#"
              className="text-gray-700 block px-4 py-2 text-sm hover:bg-blue-400 hover:text-white duration-150
              rounded-t-md
              "
            >
              Conta
            </a>
            <a
              href="#"
              className="text-gray-700 block px-4 py-2 text-sm hover:bg-blue-400 hover:text-white duration-150"
            >
              Log out
            </a>
            <a
              href="#"
              className="text-gray-700 block px-4 py-2 text-sm hover:bg-blue-400 hover:text-white duration-150 rounded-b-md"
            >
              Configurações
            </a>
          </div>
        </div>
      )}
    </div>
  );
}

export default Dropdown;
