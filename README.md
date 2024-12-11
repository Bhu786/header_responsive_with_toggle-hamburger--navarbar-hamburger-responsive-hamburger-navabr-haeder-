# header_responsive_with_toggle-hamburger--navarbar-hamburger-responsive-hamburger-navabr-haeder-

```react.js
import { useState } from "react";
import { MdOutlineMenu } from "react-icons/md";
import { Link } from "react-router-dom";
import bidVentureLogo from "../images/logo.png";

### Step:3
const Header = () => {
  const [isSidebarOpen, setIsSidebarOpen] = useState(false);

  return (
    <div className="relative">

      ### Steps:4
      {/* Mobile Menu Icon */}
      <div className="fixed top-4 left-4 z-20 md:hidden">
        <MdOutlineMenu
          onClick={() => setIsSidebarOpen(!isSidebarOpen)}
          className="text-3xl cursor-pointer"
        />
      </div>



     ### step:2
      {/* Mobile Header Logo */}
      <div className="fixed top-4 right-4 z-20 md:hidden">
        <img src={bidVentureLogo} alt="Logo" className="w-20" />
      </div>

      {/* Sidebar */}
      <aside
        className={`fixed top-0 left-0 h-full bg-white shadow-lg transition-transform transform ${
          isSidebarOpen ? "translate-x-0" : "-translate-x-full"
        } z-10 md:hidden w-3/4`}
      >
        <nav className="flex flex-col items-center space-y-4 mt-6">
          <Link
            to="/"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            Home
          </Link>
          <Link
            to="/works"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            Works
          </Link>
          <Link
            to="/services"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            Services
          </Link>
          <Link
            to="/event"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            Event
          </Link>
          <Link
            to="/aboutus"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            About Us
          </Link>
          <Link
            to="/contactus"
            className="text-lg font-semibold hover:text-indigo-600"
            onClick={() => setIsSidebarOpen(false)}
          >
            Contact Us
          </Link>
        </nav>
      </aside>



    ###  Step:1

      {/* Header for Desktop */}
      <header className="flex justify-between items-center  px-8 py-8 fixed top-0 z-10 shadow-md w-full min-h-16 bg-[#d3d7e9]">
      {/* <header className="flex justify-between items-center  px-8 py-4 fixed top-0 z-10 shadow-md w-full min-h-16 bg-gradient-to-r from-[#f3f1f4] to-[#ea1c45]"> */}
        {/* Logo */}
        <img src={bidVentureLogo} alt="Logo" className="hidden md:block w-52" />

        {/* Navigation Links */}
        <nav className="hidden md:flex items-center space-x-8">
          <Link
            to="/"
            className="text-base  font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            Home
          </Link>
          <Link
            to="/works"
            className="text-base font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            Works
          </Link>
          <Link
            to="/services"
            className="text-base font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            Services
          </Link>
          <Link
            to="/event"
            className="text-base font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            Event
          </Link>
          <Link
            to="/aboutus"
            className="text-base font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            About Us
          </Link>
          <Link
            to="/contactus"
            className="text-base font-extrabold relative after:absolute after:bottom-[-2px] after:left-0 after:w-0 after:h-0.5 after:bg-indigo-500 after:transition-all after:duration-300 hover:after:w-full"
          >
            Contact Us
          </Link>
        </nav>
      </header>




    </div>
  );
};

export default Header;

```
