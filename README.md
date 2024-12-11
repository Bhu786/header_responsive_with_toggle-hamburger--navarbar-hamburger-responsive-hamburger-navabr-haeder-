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


---
---
----

# without tailwind


```react.js

import { useState } from "react";
import { MdOutlineMenu } from "react-icons/md";
import { Link } from "react-router-dom";
import bidVentureLogo from "../images/logo.png";
import "./Header.css"; // CSS file for styles

const Header = () => {
  const [isSidebarOpen, setIsSidebarOpen] = useState(false);

  return (
    <div className="header-container">
      {/* Mobile Menu Icon */}
      <div className="menu-icon" onClick={() => setIsSidebarOpen(!isSidebarOpen)}>
        <MdOutlineMenu className="icon" />
      </div>

      {/* Mobile Header Logo */}
      <div className="mobile-logo">
        <img src={bidVentureLogo} alt="Logo" />
      </div>

      {/* Sidebar */}
      <aside className={`sidebar ${isSidebarOpen ? "open" : ""}`}>
        <nav className="sidebar-nav">
          <Link to="/" onClick={() => setIsSidebarOpen(false)}>Home</Link>
          <Link to="/works" onClick={() => setIsSidebarOpen(false)}>Works</Link>
          <Link to="/services" onClick={() => setIsSidebarOpen(false)}>Services</Link>
          <Link to="/event" onClick={() => setIsSidebarOpen(false)}>Event</Link>
          <Link to="/aboutus" onClick={() => setIsSidebarOpen(false)}>About Us</Link>
          <Link to="/contactus" onClick={() => setIsSidebarOpen(false)}>Contact Us</Link>
        </nav>
      </aside>

      {/* Desktop Header */}
      <header className="desktop-header">
        <img src={bidVentureLogo} alt="Logo" className="desktop-logo" />
        <nav className="desktop-nav">
          <Link to="/">Home</Link>
          <Link to="/works">Works</Link>
          <Link to="/services">Services</Link>
          <Link to="/event">Event</Link>
          <Link to="/aboutus">About Us</Link>
          <Link to="/contactus">Contact Us</Link>
        </nav>
      </header>
    </div>
  );
};

export default Header;





```


## css

```css
/* Global Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Arial, sans-serif;
}

/* Header Container */
.header-container {
  position: relative;
}

/* Mobile Menu Icon */
.menu-icon {
  position: fixed;
  top: 16px;
  left: 16px;
  z-index: 20;
  display: block;
  cursor: pointer;
}

.menu-icon .icon {
  font-size: 32px;
}

/* Mobile Header Logo */
.mobile-logo {
  position: fixed;
  top: 16px;
  right: 16px;
  z-index: 20;
  display: block;
}

.mobile-logo img {
  width: 80px;
}

/* Sidebar */
.sidebar {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 75%;
  max-width: 300px;
  background-color: white;
  box-shadow: 2px 0 5px rgba(0, 0, 0, 0.2);
  transform: translateX(-100%);
  transition: transform 0.3s ease-in-out;
  z-index: 10;
}

.sidebar.open {
  transform: translateX(0);
}

.sidebar-nav {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

.sidebar-nav a {
  font-size: 18px;
  font-weight: 600;
  color: black;
  text-decoration: none;
  margin: 15px 0;
  transition: color 0.2s ease-in-out;
}

.sidebar-nav a:hover {
  color: #4a90e2;
}

/* Desktop Header */
.desktop-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  position: fixed;
  top: 0;
  width: 100%;
  background-color: #d3d7e9;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  z-index: 10;
}

.desktop-logo {
  display: none;
}

.desktop-nav {
  display: none;
}

.desktop-nav a {
  font-size: 16px;
  font-weight: 700;
  color: black;
  text-decoration: none;
  margin: 0 15px;
  position: relative;
}

.desktop-nav a:hover {
  color: #4a90e2;
}

/* Hover Animation (Desktop Nav Links) */
.desktop-nav a::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0;
  height: 2px;
  background-color: #4a90e2;
  transition: width 0.3s ease-in-out;
}

.desktop-nav a:hover::after {
  width: 100%;
}

/* Media Queries */
@media (min-width: 768px) {
  .menu-icon {
    display: none;
  }

  .mobile-logo {
    display: none;
  }

  .desktop-logo {
    display: block;
    width: 150px;
  }

  .desktop-nav {
    display: flex;
  }
}


```
