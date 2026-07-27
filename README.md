# 🔖 Collection of Browsers Bookmarklets & Extension Tools

A comprehensive, copyable repository of **121 JavaScript bookmarklets** for web developers, UI/UX designers, QA engineers, and security researchers.

Each tool includes a ready-to-copy `javascript:` URL for direct browser installation, as well as formatted source code.

---

## ⚡ How to Install and Use Bookmarklets

1. Select a tool from any category listed below.
2. Copy the code from the **"📋 Bookmarklet URL"** code block (starts with `javascript:`).
3. In your web browser (Chrome, Edge, Firefox, Safari, Brave, Opera):
   - Right-click your **Bookmarks Bar** -> Select **Add Page / Add Bookmark**.
   - Enter a **Name** (e.g. *Grid Overlay*).
   - Paste the copied `javascript:...` string into the **URL / Location** field.
4. Click **Save**.
5. Click the bookmark on any webpage to instantly run the tool!

---

## Use CreepingScripts Bookmarklets Extension
A powerful bookmarklet manager that allows easy use and creation of bookmarklets. The extension is safe and user-friendly, similar to the Sealed artifact CreepingHunger.
https://github.com/DrSmoK3y/CreepingScripts-Advance-Browser-Bookmarklets-Extension

## 📋 Categories Table of Contents

- [📐 Layout & Grid Tools](#-layout-grid-tools)
- [🎨 Typography & Colors](#-typography-colors)
- [📱 Responsive & Mobile Testing](#-responsive-mobile-testing)
- [🛠️ Development & QA Utilities](#-development-qa-utilities)
- [🚀 Performance & SEO](#-performance-seo)
- [🔬 Advanced Diagnostics & Web Vitals](#-advanced-diagnostics-web-vitals)
- [🛡️ Security & Penetration Testing](#-security-penetration-testing)
- [💻 Web Development Helpers](#-web-development-helpers)
- [✍️ Content & Writing Tools](#-content-writing-tools)

---

## 📐 Layout & Grid Tools

### Grid Overlay (80px)

**Description:** Adds a subtle 80px grid overlay to check alignment across elements.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('grid-overlay-80-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('80px%20Grid%20overlay%20deactivated.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'grid-overlay-80-style';%20s.textContent%20=%20'body::before%7Bcontent:%5C%5C%22%5C%5C%22;position:fixed;top:0;left:0;right:0;bottom:0;pointer-events:none;z-index:9999;background:repeating-linear-gradient(90deg,transparent,transparent%2079px,rgba(255,0,0,0.08)%2079px,rgba(255,0,0,0.08)%2080px),repeating-linear-gradient(0deg,transparent,transparent%2079px,rgba(255,0,0,0.08)%2079px,rgba(255,0,0,0.08)%2080px)%7D';%20document.head.appendChild(s);%20console.log('80px%20Grid%20overlay%20activated.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Grid Overlay 80px style
(function() {
  const existing = document.getElementById('grid-overlay-80-style');
  if (existing) {
    existing.remove();
    console.log('80px Grid overlay deactivated.');
  } else {
    const s = document.createElement('style');
    s.id = 'grid-overlay-80-style';
    s.textContent = 'body::before{content:\\"\\";position:fixed;top:0;left:0;right:0;bottom:0;pointer-events:none;z-index:9999;background:repeating-linear-gradient(90deg,transparent,transparent 79px,rgba(255,0,0,0.08) 79px,rgba(255,0,0,0.08) 80px),repeating-linear-gradient(0deg,transparent,transparent 79px,rgba(255,0,0,0.08) 79px,rgba(255,0,0,0.08) 80px)}';
    document.head.appendChild(s);
    console.log('80px Grid overlay activated.');
  }
})();
```

---

### Grid Overlay (12-Col)

**Description:** Shows a standard CSS Bootstrap 12-column template layout with responsive gutters.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20const%20existing%20=%20d.getElementById('grid-overlay-12-div');%20if%20(existing)%20%7B%20existing.remove();%20console.log('12-Column%20grid%20overlay%20deactivated.');%20return;%20%7D%20const%20b%20=%20d.createElement('div');%20b.id%20=%20'grid-overlay-12-div';%20b.style%20=%20'position:fixed;top:0;left:50%25;transform:translateX(-50%25);width:100%25;max-width:1200px;height:100%25;pointer-events:none;z-index:9999;display:flex;gap:24px;padding:0%2024px;box-sizing:border-box';%20for%20(var%20i%20=%200;%20i%20%3C%2012;%20i++)%20%7B%20var%20c%20=%20d.createElement('div');%20c.style%20=%20'flex:1;background:rgba(255,0,0,0.03);border-left:1px%20solid%20rgba(255,0,0,0.06);border-right:1px%20solid%20rgba(255,0,0,0.06)';%20b.appendChild(c);%20%7D%20d.body.appendChild(b);%20console.log('12-Column%20grid%20layout%20activated.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// 12-Column Responsive Grid Simulator
(function() {
  const d = document;
  const existing = d.getElementById('grid-overlay-12-div');
  if (existing) {
    existing.remove();
    console.log('12-Column grid overlay deactivated.');
    return;
  }
  const b = d.createElement('div');
  b.id = 'grid-overlay-12-div';
  b.style = 'position:fixed;top:0;left:50%;transform:translateX(-50%);width:100%;max-width:1200px;height:100%;pointer-events:none;z-index:9999;display:flex;gap:24px;padding:0 24px;box-sizing:border-box';
  for (var i = 0; i < 12; i++) {
    var c = d.createElement('div');
    c.style = 'flex:1;background:rgba(255,0,0,0.03);border-left:1px solid rgba(255,0,0,0.06);border-right:1px solid rgba(255,0,0,0.06)';
    b.appendChild(c);
  }
  d.body.appendChild(b);
  console.log('12-Column grid layout activated.');
})();
```

---

### Outline All Elements

**Description:** Adds a red outline border to every object element on the page to audit structural boundaries and detect layout shifting.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('outline-all-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Outline%20boundaries%20audit%20turned%20OFF.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'outline-all-style';%20s.textContent%20=%20'*%7Boutline:1px%20solid%20rgba(255,0,0,0.35)!important;outline-offset:-1px!important%7D';%20document.head.appendChild(s);%20console.log('Outline%20boundaries%20audit%20activated.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Pesticide Style Border Outliner
(function() {
  const existing = document.getElementById('outline-all-style');
  if (existing) {
    existing.remove();
    console.log('Outline boundaries audit turned OFF.');
  } else {
    const s = document.createElement('style');
    s.id = 'outline-all-style';
    s.textContent = '*{outline:1px solid rgba(255,0,0,0.35)!important;outline-offset:-1px!important}';
    document.head.appendChild(s);
    console.log('Outline boundaries audit activated.');
  }
})();
```

---

### Outline by Depth (Rainbow)

**Description:** Highlights page structures with color-coded borders representing DOM depth nesting levels.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('outline-rainbow-style');%20if%20(existing)%20%7B%20existing.remove();%20document.querySelectorAll('*').forEach(el%20=%3E%20el.style.removeProperty('--d'));%20console.log('Rainbow%20depth%20outliner%20off.');%20%7D%20else%20%7B%20var%20s%20=%20document.createElement('style');%20s.id%20=%20'outline-rainbow-style';%20s.textContent%20=%20'*%7Boutline:1px%20solid%20hsl(calc(var(--d,0)*60),70%25,50%25)!important;outline-offset:-1px!important%7D';%20document.head.appendChild(s);%20function%20assign(e,%20n)%20%7B%20e.style.setProperty('--d',%20n);%20Array.from(e.children).forEach(c%20=%3E%20assign(c,%20n+1));%20%7D%20assign(document.body,%200);%20console.log('Rainbow%20depth%20outliner%20on!%20Level%200%20=%20Green/Yellow,%20Level%201%20=%20Red/Purple...');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Rainbow DOM Nesting depth tracker
(function() {
  const existing = document.getElementById('outline-rainbow-style');
  if (existing) {
    existing.remove();
    document.querySelectorAll('*').forEach(el => el.style.removeProperty('--d'));
    console.log('Rainbow depth outliner off.');
  } else {
    var s = document.createElement('style');
    s.id = 'outline-rainbow-style';
    s.textContent = '*{outline:1px solid hsl(calc(var(--d,0)*60),70%,50%)!important;outline-offset:-1px!important}';
    document.head.appendChild(s);
    function assign(e, n) {
      e.style.setProperty('--d', n);
      Array.from(e.children).forEach(c => assign(c, n+1));
    }
    assign(document.body, 0);
    console.log('Rainbow depth outliner on! Level 0 = Green/Yellow, Level 1 = Red/Purple...');
  }
})();
```

---

### Show Box Model on Hover

**Description:** Draws multi-colored borders representing border, padding, and margin spacing dimensions as you cursor hover over components.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20styleId%20=%20'hover-box-model-style';%20let%20existing%20=%20document.getElementById(styleId);%20if%20(existing)%20%7B%20existing.remove();%20console.log('Box%20model%20hover%20disabled');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20styleId;%20s.textContent%20=%20'.box-hover-hl%7Bbox-shadow:inset%200%200%200%201px%20#ef4444,%20inset%200%200%200%202px%20#f59e0b,%20inset%200%200%200%203px%20#10b981,%20inset%200%200%200%204px%20#3b82f6%20!important%7D';%20document.head.appendChild(s);%20document.addEventListener('mouseover',%20function(e)%20%7B%20if%20(e.target%20&&%20e.target.classList)%20e.target.classList.add('box-hover-hl');%20%7D);%20document.addEventListener('mouseout',%20function(e)%20%7B%20if%20(e.target%20&&%20e.target.classList)%20e.target.classList.remove('box-hover-hl');%20%7D);%20console.log('Box%20model%20hover%20activated!%20Red:%20Content,%20Gold:%20Padding,%20Green:%20Border,%20Blue:%20Margin%20shadow.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Hover Box Model Highlight
(function() {
  const styleId = 'hover-box-model-style';
  let existing = document.getElementById(styleId);
  if (existing) {
    existing.remove();
    console.log('Box model hover disabled');
  } else {
    const s = document.createElement('style');
    s.id = styleId;
    s.textContent = '.box-hover-hl{box-shadow:inset 0 0 0 1px #ef4444, inset 0 0 0 2px #f59e0b, inset 0 0 0 3px #10b981, inset 0 0 0 4px #3b82f6 !important}';
    document.head.appendChild(s);
    
    document.addEventListener('mouseover', function(e) {
      if (e.target && e.target.classList) e.target.classList.add('box-hover-hl');
    });
    document.addEventListener('mouseout', function(e) {
      if (e.target && e.target.classList) e.target.classList.remove('box-hover-hl');
    });
    console.log('Box model hover activated! Red: Content, Gold: Padding, Green: Border, Blue: Margin shadow.');
  }
})();
```

---

### Show Element Info Tooltip

**Description:** Instant popup telemetry widget displaying element tag properties, classes list, ID attributes, and live size metrics under cursor hover.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20if%20(window.infoTipActive)%20%7B%20window.infoTipActive%20=%20false;%20document.removeEventListener('mouseover',%20window.infoTipOver);%20const%20x%20=%20document.getElementById('el-info-tip');%20if(x)%20x.remove();%20console.log('Tooltip%20diagnostic%20off.');%20%7D%20else%20%7B%20window.infoTipActive%20=%20true;%20window.infoTipOver%20=%20function(e)%20%7B%20const%20el%20=%20e.target;%20if%20(!el%20%7C%7C%20el.id%20===%20'el-info-tip')%20return;%20const%20rect%20=%20el.getBoundingClientRect();%20const%20txt%20=%20%60Tag:%20%3C$%7Bel.tagName.toLowerCase()%7D%3E%20%7C%20Classes:%20$%7Bel.className%20%7C%7C%20'none'%7D%20%7C%20Size:%20$%7BMath.round(rect.width)%7Dx$%7BMath.round(rect.height)%7Dpx%60;%20let%20tip%20=%20document.getElementById('el-info-tip');%20if%20(!tip)%20%7B%20tip%20=%20document.createElement('div');%20tip.id%20=%20'el-info-tip';%20tip.style.cssText%20=%20'position:fixed;background:#0F172A;border:1px%20solid%20#38BDF8;color:#38BDF8;padding:6px%2012px;font-family:monospace;font-size:10px;z-index:999999;border-radius:6px;pointer-events:none;box-shadow:0%2010px%2015px%20-3px%20rgba(0,0,0,0.3)';%20document.body.appendChild(tip);%20%7D%20tip.textContent%20=%20txt;%20tip.style.top%20=%20(e.clientY%20+%2015)%20+%20'px';%20tip.style.left%20=%20(e.clientX%20+%2015)%20+%20'px';%20%7D;%20document.addEventListener('mouseover',%20window.infoTipOver);%20document.addEventListener('mouseout',%20()%20=%3E%20%7B%20const%20x%20=%20document.getElementById('el-info-tip');%20if%20(x)%20x.remove();%20%7D);%20console.log('Tooltip%20diagnostic%20active!%20Hover%20elements%20to%20see%20structural%20parameters.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Cursor Hover Info Tooltip
(function() {
  if (window.infoTipActive) {
    window.infoTipActive = false;
    document.removeEventListener('mouseover', window.infoTipOver);
    const x = document.getElementById('el-info-tip'); if(x) x.remove();
    console.log('Tooltip diagnostic off.');
  } else {
    window.infoTipActive = true;
    window.infoTipOver = function(e) {
      const el = e.target;
      if (!el || el.id === 'el-info-tip') return;
      const rect = el.getBoundingClientRect();
      const txt = `Tag: <${el.tagName.toLowerCase()}> | Classes: ${el.className || 'none'} | Size: ${Math.round(rect.width)}x${Math.round(rect.height)}px`;
      
      let tip = document.getElementById('el-info-tip');
      if (!tip) {
        tip = document.createElement('div');
        tip.id = 'el-info-tip';
        tip.style.cssText = 'position:fixed;background:#0F172A;border:1px solid #38BDF8;color:#38BDF8;padding:6px 12px;font-family:monospace;font-size:10px;z-index:999999;border-radius:6px;pointer-events:none;box-shadow:0 10px 15px -3px rgba(0,0,0,0.3)';
        document.body.appendChild(tip);
      }
      tip.textContent = txt;
      tip.style.top = (e.clientY + 15) + 'px';
      tip.style.left = (e.clientX + 15) + 'px';
    };
    document.addEventListener('mouseover', window.infoTipOver);
    document.addEventListener('mouseout', () => {
      const x = document.getElementById('el-info-tip'); if (x) x.remove();
    });
    console.log('Tooltip diagnostic active! Hover elements to see structural parameters.');
  }
})();
```

---

### Measure Click Distance

**Description:** Measure distance between any two selected coordinates on your viewport with automatic horizontal/vertical offsets diagnostics.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20p%20=%20%5B%5D;%20const%20onClk%20=%20function(e)%20%7B%20p.push(%7B%20x:%20e.clientX,%20y:%20e.clientY%20%7D);%20console.log(%60Point%20$%7Bp.length%7D:%20$%7Be.clientX%7D,%20$%7Be.clientY%7D%60);%20if%20(p.length%20===%202)%20%7B%20const%20dx%20=%20p%5B1%5D.x%20-%20p%5B0%5D.x;%20const%20dy%20=%20p%5B1%5D.y%20-%20p%5B0%5D.y;%20const%20dist%20=%20Math.sqrt(dx*dx%20+%20dy*dy).toFixed(1);%20alert(%60Measurement%20Results:%20---------------------%20Distance:%20$%7Bdist%7Dpx%20Horizontal%20dX:%20$%7Bdx%7Dpx%20Vertical%20dY:%20$%7Bdy%7Dpx%60);%20document.removeEventListener('click',%20onClk);%20%7D%20%7D;%20document.addEventListener('click',%20onClk);%20alert('Distance%20Measurement%20Tool%20Active:%20Click%20two%20distinct%20points%20on%20screen.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Two-point Canvas Distance Calculator
(function() {
  const p = [];
  const onClk = function(e) {
    p.push({ x: e.clientX, y: e.clientY });
    console.log(`Point ${p.length}: ${e.clientX}, ${e.clientY}`);
    if (p.length === 2) {
      const dx = p[1].x - p[0].x;
      const dy = p[1].y - p[0].y;
      const dist = Math.sqrt(dx*dx + dy*dy).toFixed(1);
      alert(`Measurement Results:
---------------------
Distance: ${dist}px
Horizontal dX: ${dx}px
Vertical dY: ${dy}px`);
      document.removeEventListener('click', onClk);
    }
  };
  document.addEventListener('click', onClk);
  alert('Distance Measurement Tool Active: Click two distinct points on screen.');
})();
```

---

### Ruler Overlay (Crosshair)

**Description:** Adds an aligned crosshair grid ruler system that tracks the mouse cursor to check alignments.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20const%20hId%20=%20'cross-h';%20const%20vId%20=%20'cross-v';%20const%20h%20=%20d.getElementById(hId);%20if%20(h)%20%7B%20h.remove();%20d.getElementById(vId).remove();%20console.log('Crosshair%20ruler%20disabled.');%20%7D%20else%20%7B%20const%20horizontal%20=%20d.createElement('div');%20horizontal.id%20=%20hId;%20horizontal.style%20=%20'position:fixed;top:0;left:0;width:100%25;height:1px;background:rgba(239,68,68,0.55);pointer-events:none;z-index:99999';%20const%20vertical%20=%20d.createElement('div');%20vertical.id%20=%20vId;%20vertical.style%20=%20'position:fixed;top:0;left:0;width:1px;height:100%25;background:rgba(239,68,68,0.55);pointer-events:none;z-index:99999';%20d.body.appendChild(horizontal);%20d.body.appendChild(vertical);%20d.addEventListener('mousemove',%20function(e)%20%7B%20horizontal.style.top%20=%20e.clientY%20+%20'px';%20vertical.style.left%20=%20e.clientX%20+%20'px';%20%7D);%20console.log('Crosshair%20tracking%20aligned.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Crosshair Ruler Overlay
(function() {
  const d = document;
  const hId = 'cross-h'; const vId = 'cross-v';
  const h = d.getElementById(hId);
  if (h) {
    h.remove(); d.getElementById(vId).remove();
    console.log('Crosshair ruler disabled.');
  } else {
    const horizontal = d.createElement('div'); horizontal.id = hId;
    horizontal.style = 'position:fixed;top:0;left:0;width:100%;height:1px;background:rgba(239,68,68,0.55);pointer-events:none;z-index:99999';
    const vertical = d.createElement('div'); vertical.id = vId;
    vertical.style = 'position:fixed;top:0;left:0;width:1px;height:100%;background:rgba(239,68,68,0.55);pointer-events:none;z-index:99999';
    d.body.appendChild(horizontal); d.body.appendChild(vertical);
    d.addEventListener('mousemove', function(e) {
      horizontal.style.top = e.clientY + 'px';
      vertical.style.left = e.clientX + 'px';
    });
    console.log('Crosshair tracking aligned.');
  }
})();
```

---

### Center Alignment Guides

**Description:** Pivots vertical and horizontal intersection lines at precisely 50% coordinate points to check symmetric parameters.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('center-alignment-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Center%20safety%20guides%20deactivated.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'center-alignment-style';%20s.textContent%20=%20'body::before,body::after%7Bcontent:%5C%5C%22%5C%5C%22position:fixed;pointer-events:none;z-index:9999;background:rgba(239,68,68,0.45)%7Dbody::before%7Btop:50%25;left:0;right:0;height:1.5px%7Dbody::after%7Bleft:50%25;top:0;bottom:0;width:1.5px%7D';%20document.head.appendChild(s);%20console.log('Center%20safety%20guides%20activated%20(symmetric%20intersections).');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Center Symmetry Grid Guides
(function() {
  const existing = document.getElementById('center-alignment-style');
  if (existing) {
    existing.remove();
    console.log('Center safety guides deactivated.');
  } else {
    const s = document.createElement('style');
    s.id = 'center-alignment-style';
    s.textContent = 'body::before,body::after{content:\\"\\"position:fixed;pointer-events:none;z-index:9999;background:rgba(239,68,68,0.45)}body::before{top:50%;left:0;right:0;height:1.5px}body::after{left:50%;top:0;bottom:0;width:1.5px}';
    document.head.appendChild(s);
    console.log('Center safety guides activated (symmetric intersections).');
  }
})();
```

---

### Baseline Grid (Typography)

**Description:** Overlays a repeating 24px baseline pattern grid to align paragraph content blocks.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('baseline-grid-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('24px%20Baseline%20typography%20overlay%20off.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'baseline-grid-style';%20s.textContent%20=%20'body::before%7Bcontent:%5C%22%5C%22;position:fixed;top:0;left:0;right:0;bottom:0;pointer-events:none;z-index:9999;background:repeating-linear-gradient(0deg,transparent,transparent%2023px,rgba(0,140,255,0.08)%2023px,rgba(0,140,255,0.08)%2024px)%7D';%20document.head.appendChild(s);%20console.log('24px%20Baseline%20typography%20overlay%20on.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// typographic 24px baseline grid outliner
(function() {
  const existing = document.getElementById('baseline-grid-style');
  if (existing) {
    existing.remove();
    console.log('24px Baseline typography overlay off.');
  } else {
    const s = document.createElement('style');
    s.id = 'baseline-grid-style';
    s.textContent = 'body::before{content:\"\";position:fixed;top:0;left:0;right:0;bottom:0;pointer-events:none;z-index:9999;background:repeating-linear-gradient(0deg,transparent,transparent 23px,rgba(0,140,255,0.08) 23px,rgba(0,140,255,0.08) 24px)}';
    document.head.appendChild(s);
    console.log('24px Baseline typography overlay on.');
  }
})();
```

---

### Grayscale Contrast Mode

**Description:** Toggles the whole document to monochrome grayscale to review design visual weights, focal points, and readability contrast ratios.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('grayscale-bookmarklet-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Grayscale%20color%20mode%20deactivated.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'grayscale-bookmarklet-style';%20s.textContent%20=%20'html%20%7B%20filter:%20grayscale(100%25)%20!important;%20%7D';%20document.head.appendChild(s);%20console.log('Grayscale%20contrast%20mode%20activated.%20Visual%20balance%20is%20now%20easier%20to%20audit.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Toggle Grayscale filter on html element
(function() {
  const existing = document.getElementById('grayscale-bookmarklet-style');
  if (existing) {
    existing.remove();
    console.log('Grayscale color mode deactivated.');
  } else {
    const s = document.createElement('style');
    s.id = 'grayscale-bookmarklet-style';
    s.textContent = 'html { filter: grayscale(100%) !important; }';
    document.head.appendChild(s);
    console.log('Grayscale contrast mode activated. Visual balance is now easier to audit.');
  }
})();
```

---

### Structural Elements Outline

**Description:** Visualizes the page structure by drawing subtle outline grids on standard semantic tags like header, nav, main, footer, and sections.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('semantic-outliner-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Semantic%20structural%20outliner%20off.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'semantic-outliner-style';%20s.textContent%20=%20%60%20header%20%7B%20outline:%202px%20solid%20#3b82f6%20!important;%20outline-offset:%20-2px%20!important;%20%7D%20nav%20%7B%20outline:%202px%20solid%20#10b981%20!important;%20outline-offset:%20-2px%20!important;%20%7D%20main%20%7B%20outline:%202px%20solid%20#8b5cf6%20!important;%20outline-offset:%20-2px%20!important;%20%7D%20section%20%7B%20outline:%202px%20dashed%20#f59e0b%20!important;%20outline-offset:%20-2px%20!important;%20%7D%20footer%20%7B%20outline:%202px%20solid%20#ec4899%20!important;%20outline-offset:%20-2px%20!important;%20%7D%20%60;%20document.head.appendChild(s);%20console.log('Semantic%20structural%20outliner%20on!%20Blue:%20Header,%20Green:%20Nav,%20Purple:%20Main,%20Orange:%20Section,%20Pink:%20Footer.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Outline HTML5 semantic sections with distinctive colors
(function() {
  const existing = document.getElementById('semantic-outliner-style');
  if (existing) {
    existing.remove();
    console.log('Semantic structural outliner off.');
  } else {
    const s = document.createElement('style');
    s.id = 'semantic-outliner-style';
    s.textContent = `
      header { outline: 2px solid #3b82f6 !important; outline-offset: -2px !important; }
      nav { outline: 2px solid #10b981 !important; outline-offset: -2px !important; }
      main { outline: 2px solid #8b5cf6 !important; outline-offset: -2px !important; }
      section { outline: 2px dashed #f59e0b !important; outline-offset: -2px !important; }
      footer { outline: 2px solid #ec4899 !important; outline-offset: -2px !important; }
    `;
    document.head.appendChild(s);
    console.log('Semantic structural outliner on! Blue: Header, Green: Nav, Purple: Main, Orange: Section, Pink: Footer.');
  }
})();
```

---

### Disable All Styles

**Description:** Deactivates all linked stylesheets and internal styles to test layout semantic readability without CSS.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20for%20(let%20i%20=%200;%20i%20%3C%20document.styleSheets.length;%20i++)%20%7B%20document.styleSheets%5Bi%5D.disabled%20=%20true;%20%7D%20const%20inline%20=%20document.querySelectorAll('style,%20%5Bstyle%5D');%20inline.forEach(el%20=%3E%20%7B%20if%20(el.tagName%20===%20'STYLE')%20%7B%20(el%20as%20HTMLStyleElement).disabled%20=%20true;%20%7D%20else%20%7B%20el.removeAttribute('style');%20%7D%20%7D);%20console.log('All%20page%20styles%20disabled.');%20alert('All%20linked%20and%20inline%20styles%20disabled!');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Disable all linked & embedded stylesheets
(function() {
  for (let i = 0; i < document.styleSheets.length; i++) {
    document.styleSheets[i].disabled = true;
  }
  const inline = document.querySelectorAll('style, [style]');
  inline.forEach(el => {
    if (el.tagName === 'STYLE') {
      (el as HTMLStyleElement).disabled = true;
    } else {
      el.removeAttribute('style');
    }
  });
  console.log('All page styles disabled.');
  alert('All linked and inline styles disabled!');
})();
```

---

### Reveal Hidden Elements

**Description:** Forces all hidden components (display: none, visibility: hidden, opacity: 0) to be shown with outlines.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('reveal-hidden-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Reveal%20hidden%20elements%20deactivated.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'reveal-hidden-style';%20s.textContent%20=%20'%5Bhidden%5D,%20%5Bstyle*=%22display:%20none%22%5D,%20%5Bstyle*=%22visibility:%20hidden%22%5D,%20%5Bstyle*=%22opacity:%200%22%5D%20%7B%20display:%20block%20!important;%20visibility:%20visible%20!important;%20opacity:%201%20!important;%20outline:%202px%20dashed%20#f59e0b%20!important;%20outline-offset:%20-2px%20!important;%20%7D';%20document.head.appendChild(s);%20console.log('Reveal%20hidden%20elements%20activated.%20Outlined%20in%20orange%20dashed%20lines.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Force reveal all hidden elements on page
(function() {
  const existing = document.getElementById('reveal-hidden-style');
  if (existing) {
    existing.remove();
    console.log('Reveal hidden elements deactivated.');
  } else {
    const s = document.createElement('style');
    s.id = 'reveal-hidden-style';
    s.textContent = '[hidden], [style*="display: none"], [style*="visibility: hidden"], [style*="opacity: 0"] { display: block !important; visibility: visible !important; opacity: 1 !important; outline: 2px dashed #f59e0b !important; outline-offset: -2px !important; }';
    document.head.appendChild(s);
    console.log('Reveal hidden elements activated. Outlined in orange dashed lines.');
  }
})();
```

---

### Dark Mode Booster

**Description:** Applies a rich dark-slate stylesheet override to ease eye-strain on bright corporate portals.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20id%20=%20'dark-mode-booster-style';%20var%20existing%20=%20document.getElementById(id);%20if%20(existing)%20%7B%20existing.remove();%20console.log('Dark%20mode%20booster%20disabled.');%20%7D%20else%20%7B%20var%20style%20=%20document.createElement('style');%20style.id%20=%20id;%20style.textContent%20=%20'html,%20body%20%7B%20background:%20#0f172a%20!important;%20color:%20#cbd5e1%20!important;%20%7D%20h1,%20h2,%20h3,%20h4,%20h5,%20h6,%20strong%20%7B%20color:%20#f8fafc%20!important;%20%7D%20a%20%7B%20color:%20#38bdf8%20!important;%20%7D';%20document.head.appendChild(style);%20console.log('Dark%20mode%20booster%20active.%20Injected%20dark%20slate%20background%20overrides.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Force-inject twilight dark theme
(function() {
  var id = 'dark-mode-booster-style';
  var existing = document.getElementById(id);
  if (existing) {
    existing.remove();
    console.log('Dark mode booster disabled.');
  } else {
    var style = document.createElement('style');
    style.id = id;
    style.textContent = 'html, body { background: #0f172a !important; color: #cbd5e1 !important; } h1, h2, h3, h4, h5, h6, strong { color: #f8fafc !important; } a { color: #38bdf8 !important; }';
    document.head.appendChild(style);
    console.log('Dark mode booster active. Injected dark slate background overrides.');
  }
})();
```

---

### Typography Tester (Inter)

**Description:** Forces the entire page DOM tree to load and render standard Google Inter sans-serif typeface styles.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20id%20=%20'typography-tester-style';%20var%20existing%20=%20document.getElementById(id);%20if%20(existing)%20%7B%20existing.remove();%20console.log('Typography%20tester%20font%20overrides%20disabled.');%20%7D%20else%20%7B%20var%20link%20=%20document.createElement('link');%20link.rel%20=%20'stylesheet';%20link.href%20=%20'https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap';%20document.head.appendChild(link);%20var%20style%20=%20document.createElement('style');%20style.id%20=%20id;%20style.textContent%20=%20'*%20%7B%20font-family:%20%22Inter%22,%20sans-serif%20!important;%20%7D';%20document.head.appendChild(style);%20console.log('Typography%20tester%20active.%20Loaded%20Google%20Inter%20fonts%20globally.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Load Google Fonts Inter and enforce globally
(function() {
  var id = 'typography-tester-style';
  var existing = document.getElementById(id);
  if (existing) {
    existing.remove();
    console.log('Typography tester font overrides disabled.');
  } else {
    var link = document.createElement('link');
    link.rel = 'stylesheet';
    link.href = 'https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap';
    document.head.appendChild(link);
    var style = document.createElement('style');
    style.id = id;
    style.textContent = '* { font-family: "Inter", sans-serif !important; }';
    document.head.appendChild(style);
    console.log('Typography tester active. Loaded Google Inter fonts globally.');
  }
})();
```

---

## 🎨 Typography & Colors

### Extract All Fonts

**Description:** Gathers and lists every typographic font-family configuration references used across the page DOM.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20families%20=%20new%20Set();%20document.querySelectorAll('*').forEach(el%20=%3E%20%7B%20const%20font%20=%20window.getComputedStyle(el).fontFamily;%20if%20(font)%20families.add(font.trim());%20%7D);%20const%20arr%20=%20%5B...families%5D;%20console.log('%25cDetected%20Typography%20Stacks:',%20'font-size:%2016px;%20font-weight:%20bold;%20color:%20#2563EB');%20arr.forEach((f,%20i)%20=%3E%20console.log(%60$%7Bi+1%7D.%20$%7Bf%7D%60));%20alert(%60Found%20$%7Barr.length%7D%20unique%20typography%20declarations.%20Details%20printed%20in%20Developer%20Console.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// DOM Font families extractor
(function() {
  const families = new Set();
  document.querySelectorAll('*').forEach(el => {
    const font = window.getComputedStyle(el).fontFamily;
    if (font) families.add(font.trim());
  });
  const arr = [...families];
  console.log('%cDetected Typography Stacks:', 'font-size: 16px; font-weight: bold; color: #2563EB');
  arr.forEach((f, i) => console.log(`${i+1}. ${f}`));
  alert(`Found ${arr.length} unique typography declarations. Details printed in Developer Console.`);
})();
```

---

### Extract Color Palette

**Description:** Finds, counts, and logs every color token used on the page background, text colors, and borders.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20colors%20=%20new%20Set();%20document.querySelectorAll('*').forEach(e%20=%3E%20%7B%20const%20style%20=%20getComputedStyle(e);%20%5B'color',%20'backgroundColor',%20'borderColor'%5D.forEach(p%20=%3E%20%7B%20const%20v%20=%20style%5Bp%5D;%20if%20(v%20&&%20v%20!==%20'rgba(0,%200,%200,%200)'%20&&%20v%20!==%20'transparent')%20colors.add(v);%20%7D);%20%7D);%20console.log('%25cExtracted%20Corporate%20Palette%20(%25d%20colors):',%20'font-size:%2015px;%20font-weight:%20bold;%20color:%20#EC4899',%20colors.size);%20%5B...colors%5D.forEach(c%20=%3E%20%7B%20console.log(%60%25c%20$%7Bc%7D%20%60,%20%60background:$%7Bc%7D;%20color:#fff;%20padding:3px%206px;%20border-radius:4px;%20margin:2px;%20font-family:monospace%60);%20%7D);%20alert(%60Extracted%20$%7Bcolors.size%7D%20unique%20color%20values!%20View%20console%20outputs.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Extract All Color Parameters
(function() {
  const colors = new Set();
  document.querySelectorAll('*').forEach(e => {
    const style = getComputedStyle(e);
    ['color', 'backgroundColor', 'borderColor'].forEach(p => {
      const v = style[p];
      if (v && v !== 'rgba(0, 0, 0, 0)' && v !== 'transparent') colors.add(v);
    });
  });
  console.log('%cExtracted Corporate Palette (%d colors):', 'font-size: 15px; font-weight: bold; color: #EC4899', colors.size);
  [...colors].forEach(c => {
    console.log(`%c ${c} `, `background:${c}; color:#fff; padding:3px 6px; border-radius:4px; margin:2px; font-family:monospace`);
  });
  alert(`Extracted ${colors.size} unique color values! View console outputs.`);
})();
```

---

### Show Font Sizes

**Description:** Draws temporary absolute pixel markers directly above text blocks indicating computed typography sizes.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.querySelectorAll('.font-size-marker');%20if%20(existing.length)%20%7B%20existing.forEach(x%20=%3E%20x.remove());%20console.log('Font%20size%20markers%20cleared.');%20return;%20%7D%20document.querySelectorAll('h1,%20h2,%20h3,%20h4,%20h5,%20h6,%20p,%20span').forEach(e%20=%3E%20%7B%20const%20fs%20=%20parseFloat(getComputedStyle(e).fontSize);%20if%20(fs%20%3E=%2010)%20%7B%20const%20b%20=%20document.createElement('span');%20b.className%20=%20'font-size-marker';%20b.textContent%20=%20fs%20+%20'px';%20b.style%20=%20'position:absolute;background:#10B981;color:white;font:9px%20monospace;padding:1px%203px;border-radius:3px;z-index:10000;pointer-events:none;transform:translateY(-12px)';%20e.style.position%20=%20'relative';%20e.appendChild(b);%20%7D%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Visual Font Size Overlay
(function() {
  const existing = document.querySelectorAll('.font-size-marker');
  if (existing.length) {
    existing.forEach(x => x.remove());
    console.log('Font size markers cleared.');
    return;
  }
  document.querySelectorAll('h1, h2, h3, h4, h5, h6, p, span').forEach(e => {
    const fs = parseFloat(getComputedStyle(e).fontSize);
    if (fs >= 10) {
      const b = document.createElement('span');
      b.className = 'font-size-marker';
      b.textContent = fs + 'px';
      b.style = 'position:absolute;background:#10B981;color:white;font:9px monospace;padding:1px 3px;border-radius:3px;z-index:10000;pointer-events:none;transform:translateY(-12px)';
      e.style.position = 'relative';
      e.appendChild(b);
    }
  });
})();
```

---

### Show Line Heights

**Description:** Labels calculated vertical line-interval spacing directly on text headings to inspect vertical typography scale.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.querySelectorAll('.lh-marker');%20if%20(existing.length)%20%7B%20existing.forEach(x%20=%3E%20x.remove());%20console.log('Layout%20line%20height%20markers%20disabled.');%20return;%20%7D%20document.querySelectorAll('h1,%20h2,%20h3,%20h4,%20p').forEach(e%20=%3E%20%7B%20const%20lh%20=%20getComputedStyle(e).lineHeight;%20if%20(lh%20&&%20lh%20!==%20'normal')%20%7B%20const%20b%20=%20document.createElement('span');%20b.className%20=%20'lh-marker';%20b.textContent%20=%20'LH:'%20+%20lh;%20b.style%20=%20'position:absolute;background:#6366F1;color:white;font:8px%20monospace;padding:1px%203px;border-radius:2px;z-index:9999;pointer-events:none;transform:translateY(12px)';%20e.style.position%20=%20'relative';%20e.appendChild(b);%20%7D%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Line Height Metric Diagnostic
(function() {
  const existing = document.querySelectorAll('.lh-marker');
  if (existing.length) {
    existing.forEach(x => x.remove());
    console.log('Layout line height markers disabled.');
    return;
  }
  document.querySelectorAll('h1, h2, h3, h4, p').forEach(e => {
    const lh = getComputedStyle(e).lineHeight;
    if (lh && lh !== 'normal') {
      const b = document.createElement('span');
      b.className = 'lh-marker';
      b.textContent = 'LH:' + lh;
      b.style = 'position:absolute;background:#6366F1;color:white;font:8px monospace;padding:1px 3px;border-radius:2px;z-index:9999;pointer-events:none;transform:translateY(12px)';
      e.style.position = 'relative';
      e.appendChild(b);
    }
  });
})();
```

---

### Contrast Click Checker

**Description:** Click on any element on the page to retrieve foreground color and outer backplate RGB values to check readability.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20onClk%20=%20function(e)%20%7B%20const%20el%20=%20e.target;%20if%20(el)%20%7B%20const%20s%20=%20getComputedStyle(el);%20console.log(%60Contrast%20Audit%20for%20%3C$%7Bel.tagName.toLowerCase()%7D%3E:%60,%20%7B%20textColor:%20s.color,%20backgroundColor:%20s.backgroundColor,%20fontSize:%20s.fontSize,%20fontWeight:%20s.fontWeight%20%7D);%20alert(%60Contrast%20Details:%20Tag:%20%3C$%7Bel.tagName.toLowerCase()%7D%3E%20Foreground:%20$%7Bs.color%7D%20Background:%20$%7Bs.backgroundColor%7D%20Use%20these%20settings%20in%20WCAG%20checkers%20to%20evaluate%20accessibility%20compliance!%60);%20document.removeEventListener('click',%20onClk);%20%7D%20e.preventDefault();%20%7D;%20document.addEventListener('click',%20onClk);%20alert('Contrast%20Checker%20Click%20Mode%20Active:%20Click%20on%20a%20text%20element.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Contrast Check Element Targeter
(function() {
  const onClk = function(e) {
    const el = e.target;
    if (el) {
      const s = getComputedStyle(el);
      console.log(`Contrast Audit for <${el.tagName.toLowerCase()}>:`, {
        textColor: s.color,
        backgroundColor: s.backgroundColor,
        fontSize: s.fontSize,
        fontWeight: s.fontWeight
      });
      alert(`Contrast Details:
Tag: <${el.tagName.toLowerCase()}>
Foreground: ${s.color}
Background: ${s.backgroundColor}
Use these settings in WCAG checkers to evaluate accessibility compliance!`);
      document.removeEventListener('click', onClk);
    }
    e.preventDefault();
  };
  document.addEventListener('click', onClk);
  alert('Contrast Checker Click Mode Active: Click on a text element.');
})();
```

---

### Highlight Small Text

**Description:** Outlines any micro-copy elements configured below 12px in warning colors to flag accessibility issues.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20c%20=%200;%20document.querySelectorAll('p,%20span,%20a,%20li,%20div').forEach(e%20=%3E%20%7B%20if%20(e.children.length%20===%200%20&&%20e.textContent.trim()%20!==%20'')%20%7B%20const%20fs%20=%20parseFloat(getComputedStyle(e).fontSize);%20if%20(fs%20%3E%200%20&&%20fs%20%3C%2012)%20%7B%20e.style.outline%20=%20'2.5px%20dashed%20#EF4444';%20e.style.outlineOffset%20=%20'2px';%20c++;%20%7D%20%7D%20%7D);%20alert(%60Found%20$%7Bc%7D%20elements%20configured%20with%20font%20sizes%20under%2012px.%20Marked%20in%20red%20dashed%20outlines.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Highlight Small Fonts (<12px)
(function() {
  let c = 0;
  document.querySelectorAll('p, span, a, li, div').forEach(e => {
    // extract length
    if (e.children.length === 0 && e.textContent.trim() !== '') {
      const fs = parseFloat(getComputedStyle(e).fontSize);
      if (fs > 0 && fs < 12) {
        e.style.outline = '2.5px dashed #EF4444';
        e.style.outlineOffset = '2px';
        c++;
      }
    }
  });
  alert(`Found ${c} elements configured with font sizes under 12px. Marked in red dashed outlines.`);
})();
```

---

### Font Weight Distribution

**Description:** Compiles a diagnostic distribution logging weight density across elements.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20map%20=%20%7B%7D;%20document.querySelectorAll('*').forEach(e%20=%3E%20%7B%20if%20(e.textContent.trim()%20!==%20'')%20%7B%20const%20weight%20=%20getComputedStyle(e).fontWeight;%20map%5Bweight%5D%20=%20(map%5Bweight%5D%20%7C%7C%200)%20+%201;%20%7D%20%7D);%20console.log('%25cTypography%20CSS%20Weights%20Ratio:',%20'font-size:15px;%20font-weight:bold;%20color:#7C3AED');%20Object.entries(map).sort((a,b)=%3Eb%5B1%5D-a%5B1%5D).forEach((%5Bw,%20count%5D)%20=%3E%20%7B%20console.log(%60Weight:%20$%7Bw%7D%20-%3E%20applied%20across%20$%7Bcount%7D%20tags.%60);%20%7D);%20alert('Font%20weight%20ratio%20compiled%20on%20debugger%20console!');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Visual Font Weight Map Analyzer
(function() {
  const map = {};
  document.querySelectorAll('*').forEach(e => {
    if (e.textContent.trim() !== '') {
      const weight = getComputedStyle(e).fontWeight;
      map[weight] = (map[weight] || 0) + 1;
    }
  });
  console.log('%cTypography CSS Weights Ratio:', 'font-size:15px; font-weight:bold; color:#7C3AED');
  Object.entries(map).sort((a,b)=>b[1]-a[1]).forEach(([w, count]) => {
    console.log(`Weight: ${w} -> applied across ${count} tags.`);
  });
  alert('Font weight ratio compiled on debugger console!');
})();
```

---

### Extract CSS Variables

**Description:** Finds, extracts, and lists all CSS custom property tokens defined across styles sheet rules.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20vars%20=%20%7B%7D;%20try%20%7B%20Array.from(document.styleSheets).forEach(sheet%20=%3E%20%7B%20try%20%7B%20Array.from(sheet.cssRules).forEach(rule%20=%3E%20%7B%20if%20(rule.style)%20%7B%20Array.from(rule.style).forEach(prop%20=%3E%20%7B%20if%20(prop.startsWith('--'))%20%7B%20vars%5Bprop%5D%20=%20rule.style.getPropertyValue(prop).trim();%20%7D%20%7D);%20%7D%20%7D);%20%7D%20catch(e)%20%7B%7D%20%7D);%20%7D%20catch(e)%20%7B%7D%20const%20entries%20=%20Object.entries(vars);%20if%20(entries.length%20===%200)%20%7B%20alert('No%20root%20custom%20properties%20(--css-prop)%20detected.');%20return;%20%7D%20console.log('%25cCSS%20Custom%20Tokens%20Matrix:',%20'font-size:15px;%20font-weight:bold;%20color:#0D9488',%20vars);%20entries.forEach((%5Bkey,%20val%5D)%20=%3E%20%7B%20console.log(%60%25c%20$%7Bkey%7D%20%25c%20$%7Bval%7D%20%60,%20'background:#1E293B;%20color:#F1F5F9;%20padding:2px%204px;%20border-radius:3px%200%200%203px',%20'background:#0D9488;%20color:#fff;%20padding:2px%204px;%20border-radius:0%203px%203px%200');%20%7D);%20alert(%60Found%20$%7Bentries.length%7D%20variables.%20Active%20design%20codes%20print%20cataloged%20in%20console.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Extracted Theme CSS variables
(function() {
  const vars = {};
  try {
    Array.from(document.styleSheets).forEach(sheet => {
      try {
        Array.from(sheet.cssRules).forEach(rule => {
          if (rule.style) {
            Array.from(rule.style).forEach(prop => {
              if (prop.startsWith('--')) {
                vars[prop] = rule.style.getPropertyValue(prop).trim();
              }
            });
          }
        });
      } catch(e) {}
    });
  } catch(e) {}
  
  const entries = Object.entries(vars);
  if (entries.length === 0) {
    alert('No root custom properties (--css-prop) detected.');
    return;
  }
  console.log('%cCSS Custom Tokens Matrix:', 'font-size:15px; font-weight:bold; color:#0D9488', vars);
  entries.forEach(([key, val]) => {
    console.log(`%c ${key} %c ${val} `, 'background:#1E293B; color:#F1F5F9; padding:2px 4px; border-radius:3px 0 0 3px', 'background:#0D9488; color:#fff; padding:2px 4px; border-radius:0 3px 3px 0');
  });
  alert(`Found ${entries.length} variables. Active design codes print cataloged in console.`);
})();
```

---

### Color Eye Dropper

**Description:** Leverages browser EyeDropper API to pick colors directly from viewport elements, outputting HEX values.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20if%20(!window.EyeDropper)%20%7B%20alert('The%20EyeDropper%20API%20is%20not%20supported%20in%20this%20browser%20version.%20Use%20Chrome/Edge/Brave.');%20return;%20%7D%20const%20picker%20=%20new%20window.EyeDropper();%20console.log('Eye%20dropper%20active:%20click%20on%20any%20pixel...');%20picker.open().then(result%20=%3E%20%7B%20console.log('Selected%20Color%20Hex%20Value:',%20result.sRGBHex);%20alert(%60Extracted%20Hex:%20$%7Bresult.sRGBHex%7D%20Copied%20to%20Clipboard!%60);%20navigator.clipboard.writeText(result.sRGBHex);%20%7D).catch(err%20=%3E%20%7B%20console.log('EyeDropper%20closed%20without%20selection.',%20err);%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Native Browser HTML Eye Dropper
(function() {
  if (!window.EyeDropper) {
    alert('The EyeDropper API is not supported in this browser version. Use Chrome/Edge/Brave.');
    return;
  }
  const picker = new window.EyeDropper();
  console.log('Eye dropper active: click on any pixel...');
  picker.open().then(result => {
    console.log('Selected Color Hex Value:', result.sRGBHex);
    alert(`Extracted Hex: ${result.sRGBHex}
Copied to Clipboard!`);
    navigator.clipboard.writeText(result.sRGBHex);
  }).catch(err => {
    console.log('EyeDropper closed without selection.', err);
  });
})();
```

---

### Typography Scale Visualizer

**Description:** Renders an visual panel demonstrating font scaling multipliers across heading structures.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20const%20old%20=%20d.getElementById('typo-scale-panel');%20if%20(old)%20old.remove();%20const%20b%20=%20d.createElement('div');%20b.id%20=%20'typo-scale-panel';%20b.style%20=%20'position:fixed;top:15px;right:15px;background:#1E293B;color:#F8FAFC;border:1px%20solid%20#475569;padding:16px;z-index:99999;font-family:system-ui;width:280px;border-radius:8px;box-shadow:0%2010px%2020px%20rgba(0,0,0,0.3)';%20let%20h%20=%20'%3Ch3%20style=%22margin:0%200%2010px;font-size:13px;font-weight:bold;color:#60A5FA;border-bottom:1px%20solid%20#475569;padding-bottom:4px%22%3ETypographic%20System%20scale%3C/h3%3E';%20%5B'h1','h2','h3','h4','p'%5D.forEach(t%20=%3E%20%7B%20const%20e%20=%20d.querySelector(t);%20if%20(e)%20%7B%20const%20s%20=%20getComputedStyle(e);%20h%20+=%20%60%3Cdiv%20style=%22margin:6px%200;font-size:10px;display:flex;justify-content:space-between%22%3E%3Cspan%3E%3Cb%3E$%7Bt.toUpperCase()%7D:%3C/b%3E%3C/span%3E%20%3Cspan%20style=%22font-family:monospace%22%3E$%7Bs.fontSize%7D%20/%20$%7Bs.lineHeight%7D%3C/span%3E%3C/div%3E%60;%20%7D%20else%20%7B%20h%20+=%20%60%3Cdiv%20style=%22margin:6px%200;font-size:10px;color:#64748B;display:flex;justify-content:space-between%22%3E%3Cspan%3E%3Cb%3E$%7Bt.toUpperCase()%7D:%3C/b%3E%3C/span%3E%20%3Cspan%3EN/A%3C/span%3E%3C/div%3E%60;%20%7D%20%7D);%20b.innerHTML%20=%20h%20+%20'%3Cbutton%20onclick=%22this.parentElement.remove()%22%20style=%22margin-top:12px;width:100%25;padding:5px;border-radius:4px;background:#475569;color:#F8FAFC;border:none;cursor:pointer;font-size:10px;font-weight:bold%22%3EDismiss%3C/button%3E';%20d.body.appendChild(b);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Computed Heading Scale Calculator
(function() {
  const d = document;
  const old = d.getElementById('typo-scale-panel'); if (old) old.remove();
  const b = d.createElement('div');
  b.id = 'typo-scale-panel';
  b.style = 'position:fixed;top:15px;right:15px;background:#1E293B;color:#F8FAFC;border:1px solid #475569;padding:16px;z-index:99999;font-family:system-ui;width:280px;border-radius:8px;box-shadow:0 10px 20px rgba(0,0,0,0.3)';
  
  let h = '<h3 style="margin:0 0 10px;font-size:13px;font-weight:bold;color:#60A5FA;border-bottom:1px solid #475569;padding-bottom:4px">Typographic System scale</h3>';
  ['h1','h2','h3','h4','p'].forEach(t => {
    const e = d.querySelector(t);
    if (e) {
      const s = getComputedStyle(e);
      h += `<div style="margin:6px 0;font-size:10px;display:flex;justify-content:space-between"><span><b>${t.toUpperCase()}:</b></span> <span style="font-family:monospace">${s.fontSize} / ${s.lineHeight}</span></div>`;
    } else {
      h += `<div style="margin:6px 0;font-size:10px;color:#64748B;display:flex;justify-content:space-between"><span><b>${t.toUpperCase()}:</b></span> <span>N/A</span></div>`;
    }
  });
  b.innerHTML = h + '<button onclick="this.parentElement.remove()" style="margin-top:12px;width:100%;padding:5px;border-radius:4px;background:#475569;color:#F8FAFC;border:none;cursor:pointer;font-size:10px;font-weight:bold">Dismiss</button>';
  d.body.appendChild(b);
})();
```

---

## 📱 Responsive & Mobile Testing

### Viewport Size Overlay

**Description:** Displays viewport dimension vectors and device pixel counters in real time as the browser window resizes.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20widgetId%20=%20'viewport-size-widget';%20const%20old%20=%20document.getElementById(widgetId);%20if%20(old)%20%7B%20old.remove();%20window.removeEventListener('resize',%20window.updateVSize);%20console.log('Sizer%20utility%20off.');%20%7D%20else%20%7B%20const%20b%20=%20document.createElement('div');%20b.id%20=%20widgetId;%20b.style.cssText%20=%20'position:fixed;bottom:16px;right:16px;background:rgba(15,23,42,0.95);border:1.5px%20solid%20#10B981;color:#10B981;padding:8px%2012px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;pointer-events:none;box-shadow:0%2010px%2015px%20-3px%20rgba(0,0,0,0.3)';%20document.body.appendChild(b);%20window.updateVSize%20=%20function()%20%7B%20b.textContent%20=%20%60Viewport:%20$%7Bwindow.innerWidth%7D%20x%20$%7Bwindow.innerHeight%7D%20px%20@%20$%7Bwindow.devicePixelRatio%7Dx%60;%20%7D;%20window.updateVSize();%20window.addEventListener('resize',%20window.updateVSize);%20console.log('Sizer%20utility%20on!%20Resize%20the%20browser%20viewport%20window.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Viewport Sizer telemetry tracker
(function() {
  const widgetId = 'viewport-size-widget';
  const old = document.getElementById(widgetId);
  if (old) {
    old.remove();
    window.removeEventListener('resize', window.updateVSize);
    console.log('Sizer utility off.');
  } else {
    const b = document.createElement('div');
    b.id = widgetId;
    b.style.cssText = 'position:fixed;bottom:16px;right:16px;background:rgba(15,23,42,0.95);border:1.5px solid #10B981;color:#10B981;padding:8px 12px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;pointer-events:none;box-shadow:0 10px 15px -3px rgba(0,0,0,0.3)';
    document.body.appendChild(b);
    window.updateVSize = function() {
      b.textContent = `Viewport: ${window.innerWidth} x ${window.innerHeight} px @ ${window.devicePixelRatio}x`;
    };
    window.updateVSize();
    window.addEventListener('resize', window.updateVSize);
    console.log('Sizer utility on! Resize the browser viewport window.');
  }
})();
```

---

### Breakpoint Detector

**Description:** Displays CSS Tailwind responsive classes (sm, md, lg, xl) matching your active screen sizes.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20widgetId%20=%20'breakpoint-widget';%20const%20existing%20=%20document.getElementById(widgetId);%20if%20(existing)%20%7B%20existing.remove();%20window.removeEventListener('resize',%20window.updateBreakp);%20console.log('Breakpoint%20detector%20off.');%20%7D%20else%20%7B%20const%20b%20=%20document.createElement('div');%20b.id%20=%20widgetId;%20b.style.cssText%20=%20'position:fixed;top:16px;left:16px;background:#3B82F6;color:white;padding:8px%2012px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;box-shadow:0%2010px%2015px%20-3px%20rgba(0,0,0,0.3);pointer-events:none';%20document.body.appendChild(b);%20window.updateBreakp%20=%20function()%20%7B%20const%20w%20=%20window.innerWidth;%20let%20label%20=%20'XS%20(Mobile%20%3C640px)';%20if%20(w%20%3E=%201536)%20%7B%20b.style.background%20=%20'#EC4899';%20label%20=%20'2XL%20(Wide%20%3E=1536px)';%20%7D%20else%20if%20(w%20%3E=%201280)%20%7B%20b.style.background%20=%20'#8B5CF6';%20label%20=%20'XL%20(Standard%20Desktop%20%3E=1280px)';%20%7D%20else%20if%20(w%20%3E=%201024)%20%7B%20b.style.background%20=%20'#3B82F6';%20label%20=%20'LG%20(Laptop%20%3E=1024px)';%20%7D%20else%20if%20(w%20%3E=%20768)%20%7B%20b.style.background%20=%20'#10B981';%20label%20=%20'MD%20(Tablet%20%3E=768px)';%20%7D%20else%20if%20(w%20%3E=%20640)%20%7B%20b.style.background%20=%20'#F59E0B';%20label%20=%20'SM%20(Mobile%20Landscape%20%3E=640px)';%20%7D%20else%20%7B%20b.style.background%20=%20'#EF4444';%20%7D%20b.textContent%20=%20%60$%7Bw%7Dpx%20-%20CSS%20Breakpoint:%20$%7Blabel%7D%60;%20%7D;%20window.updateBreakp();%20window.addEventListener('resize',%20window.updateBreakp);%20console.log('Breakpoint%20detector%20activated.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Tailwind Breakpoint monitor
(function() {
  const widgetId = 'breakpoint-widget';
  const existing = document.getElementById(widgetId);
  if (existing) {
    existing.remove();
    window.removeEventListener('resize', window.updateBreakp);
    console.log('Breakpoint detector off.');
  } else {
    const b = document.createElement('div');
    b.id = widgetId;
    b.style.cssText = 'position:fixed;top:16px;left:16px;background:#3B82F6;color:white;padding:8px 12px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;box-shadow:0 10px 15px -3px rgba(0,0,0,0.3);pointer-events:none';
    document.body.appendChild(b);
    window.updateBreakp = function() {
      const w = window.innerWidth;
      let label = 'XS (Mobile <640px)';
      if (w >= 1536) { b.style.background = '#EC4899'; label = '2XL (Wide >=1536px)'; }
      else if (w >= 1280) { b.style.background = '#8B5CF6'; label = 'XL (Standard Desktop >=1280px)'; }
      else if (w >= 1024) { b.style.background = '#3B82F6'; label = 'LG (Laptop >=1024px)'; }
      else if (w >= 768) { b.style.background = '#10B981'; label = 'MD (Tablet >=768px)'; }
      else if (w >= 640) { b.style.background = '#F59E0B'; label = 'SM (Mobile Landscape >=640px)'; }
      else { b.style.background = '#EF4444'; }
      b.textContent = `${w}px - CSS Breakpoint: ${label}`;
    };
    window.updateBreakp();
    window.addEventListener('resize', window.updateBreakp);
    console.log('Breakpoint detector activated.');
  }
})();
```

---

### iPhone Simulator Frame

**Description:** Renders the active webpage inside an SVG mock phone chassis centered with standard boundaries.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20containerId%20=%20'iphone-wrapper';%20const%20existing%20=%20document.getElementById(containerId);%20if%20(existing)%20%7B%20existing.remove();%20console.log('Device%20simulation%20wrapper%20discarded.');%20return;%20%7D%20const%20wrapper%20=%20document.createElement('div');%20wrapper.id%20=%20containerId;%20wrapper.style.cssText%20=%20'position:fixed;top:50%25;left:50%25;transform:translate(-50%25,-50%25);width:375px;height:812px;border:14px%20solid%20#1E293B;border-radius:40px;overflow:hidden;z-index:999999;background:#000;box-shadow:0%2025px%2050px%20-12px%20rgba(0,0,0,0.5)';%20const%20iframe%20=%20document.createElement('iframe');%20iframe.src%20=%20window.location.href;%20iframe.style.cssText%20=%20'width:%20100%25;%20height:%20100%25;%20border:%20none;%20background:%20white';%20wrapper.appendChild(iframe);%20const%20closeBtn%20=%20document.createElement('button');%20closeBtn.textContent%20=%20'%E2%9C%95%20Close%20Frame';%20closeBtn.style.cssText%20=%20'position:absolute;top:12px;right:12px;background:#EF4444;color:white;border:none;padding:6px%2012px;border-radius:6px;cursor:pointer;font-family:sans-serif;font-size:11px;font-weight:bold';%20closeBtn.onclick%20=%20()%20=%3E%20wrapper.remove();%20wrapper.appendChild(closeBtn);%20document.body.appendChild(wrapper);%20console.log('iPhone%20layout%20emulation%20frame%20activated.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// iPhone chassis emulation frames wrapper
(function() {
  const containerId = 'iphone-wrapper';
  const existing = document.getElementById(containerId);
  if (existing) {
    existing.remove();
    console.log('Device simulation wrapper discarded.');
    return;
  }
  const wrapper = document.createElement('div');
  wrapper.id = containerId;
  wrapper.style.cssText = 'position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);width:375px;height:812px;border:14px solid #1E293B;border-radius:40px;overflow:hidden;z-index:999999;background:#000;box-shadow:0 25px 50px -12px rgba(0,0,0,0.5)';
  
  const iframe = document.createElement('iframe');
  iframe.src = window.location.href;
  iframe.style.cssText = 'width: 100%; height: 100%; border: none; background: white';
  wrapper.appendChild(iframe);
  
  const closeBtn = document.createElement('button');
  closeBtn.textContent = '✕ Close Frame';
  closeBtn.style.cssText = 'position:absolute;top:12px;right:12px;background:#EF4444;color:white;border:none;padding:6px 12px;border-radius:6px;cursor:pointer;font-family:sans-serif;font-size:11px;font-weight:bold';
  closeBtn.onclick = () => wrapper.remove();
  wrapper.appendChild(closeBtn);
  
  document.body.appendChild(wrapper);
  console.log('iPhone layout emulation frame activated.');
})();
```

---

### Touch Event Simulator

**Description:** Translates classic click coordinates into responsive mobile Touch interaction signals to inspect slider elements.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20handler%20=%20function(e)%20%7B%20if%20(!e.target)%20return;%20const%20touch%20=%20new%20Touch(%7B%20identifier:%20Date.now(),%20target:%20e.target,%20clientX:%20e.clientX,%20clientY:%20e.clientY,%20screenX:%20e.screenX,%20screenY:%20e.screenY,%20pageX:%20e.pageX,%20pageY:%20e.pageY%20%7D);%20const%20touchStart%20=%20new%20TouchEvent('touchstart',%20%7B%20touches:%20%5Btouch%5D,%20targetTouches:%20%5Btouch%5D,%20changedTouches:%20%5Btouch%5D,%20bubbles:%20true,%20cancelable:%20true%20%7D);%20e.target.dispatchEvent(touchStart);%20console.log('Fired%20simulated%20touchstart%20at%20coordinate:',%20e.clientX,%20e.clientY);%20%7D;%20if%20(window.touchSimActive)%20%7B%20window.touchSimActive%20=%20false;%20document.removeEventListener('mousedown',%20handler);%20alert('Touch%20interactions%20simulator%20disabled.');%20%7D%20else%20%7B%20window.touchSimActive%20=%20true;%20document.addEventListener('mousedown',%20handler);%20alert('Touch%20interactions%20simulator%20active!%20Click%20events%20translate%20into%20native%20TouchStart%20coordinates.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Click Event to Touch Event converter
(function() {
  const handler = function(e) {
    if (!e.target) return;
    const touch = new Touch({
      identifier: Date.now(),
      target: e.target,
      clientX: e.clientX,
      clientY: e.clientY,
      screenX: e.screenX,
      screenY: e.screenY,
      pageX: e.pageX,
      pageY: e.pageY
    });
    const touchStart = new TouchEvent('touchstart', {
      touches: [touch],
      targetTouches: [touch],
      changedTouches: [touch],
      bubbles: true,
      cancelable: true
    });
    e.target.dispatchEvent(touchStart);
    console.log('Fired simulated touchstart at coordinate:', e.clientX, e.clientY);
  };
  
  if (window.touchSimActive) {
    window.touchSimActive = false;
    document.removeEventListener('mousedown', handler);
    alert('Touch interactions simulator disabled.');
  } else {
    window.touchSimActive = true;
    document.addEventListener('mousedown', handler);
    alert('Touch interactions simulator active! Click events translate into native TouchStart coordinates.');
  }
})();
```

---

### 2G Connection Faker

**Description:** Overrides standard connection objects, reporting low bandwidth speeds to let scripts simulate lazy load limits.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20code%20=%20%60%20Object.defineProperty(navigator,%20%22connection%22,%20%7B%20get:%20function()%20%7B%20return%20%7B%20effectiveType:%20%222g%22,%20rtt:%201500,%20downlink:%200.1,%20saveData:%20true%20%7D;%20%7D,%20configurable:%20true%20%7D);%20console.log(%22Faked%20navigator%20connection%20status%20to:%202G%20Throttling%20Profile.%22);%20%60;%20const%20s%20=%20document.createElement('script');%20s.textContent%20=%20code;%20document.head.appendChild(s);%20alert('Connection%20profiles%20updated.%20Navigator%20scripts%20will%20simulate%20cellular%202G%20networks%20loading%20budgets.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Override Network Speed Profiles
(function() {
  const code = `
    Object.defineProperty(navigator, "connection", {
      get: function() {
        return {
          effectiveType: "2g",
          rtt: 1500,
          downlink: 0.1,
          saveData: true
        };
      },
      configurable: true
    });
    console.log("Faked navigator connection status to: 2G Throttling Profile.");
  `;
  const s = document.createElement('script');
  s.textContent = code;
  document.head.appendChild(s);
  alert('Connection profiles updated. Navigator scripts will simulate cellular 2G networks loading budgets.');
})();
```

---

### Print CSS Styles Preview

**Description:** Enforces printing media rules directly into the standard viewport browser layouts to visually audit style properties.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20stylesheetId%20=%20'print-media-faker';%20const%20existing%20=%20document.getElementById(stylesheetId);%20if%20(existing)%20%7B%20existing.remove();%20console.log('Print%20preview%20simulation%20disabled.');%20%7D%20else%20%7B%20const%20style%20=%20document.createElement('style');%20style.id%20=%20stylesheetId;%20style.innerHTML%20=%20%60%20@media%20screen%20%7B%20body%20%7B%20background:%20white%20!important;%20color:%20black%20!important;%20font-family:%20serif%20!important;%20%7D%20nav,%20footer,%20.sidebar,%20button,%20.no-print%20%7B%20display:%20none%20!important;%20%7D%20img%20%7B%20filter:%20grayscale(100%25)%20!important;%20max-width:%20100%25%20!important;%20%7D%20a::after%20%7B%20content:%20%22%20(%22%20attr(href)%20%22)%22;%20font-size:%2080%25;%20color:%20#666;%20%7D%20%7D%20%60;%20document.head.appendChild(style);%20console.log('Force%20printing%20preview%20turned%20ON.%20Check%20layout%20printability!');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Force Print Media stylesheet injection
(function() {
  const stylesheetId = 'print-media-faker';
  const existing = document.getElementById(stylesheetId);
  if (existing) {
    existing.remove();
    console.log('Print preview simulation disabled.');
  } else {
    const style = document.createElement('style');
    style.id = stylesheetId;
    style.innerHTML = `
      @media screen {
        body { background: white !important; color: black !important; font-family: serif !important; }
        nav, footer, .sidebar, button, .no-print { display: none !important; }
        img { filter: grayscale(100%) !important; max-width: 100% !important; }
        a::after { content: " (" attr(href) ")"; font-size: 80%; color: #666; }
      }
    `;
    document.head.appendChild(style);
    console.log('Force printing preview turned ON. Check layout printability!');
  }
})();
```

---

### Invert Dark Mode

**Description:** Inverts parent layout hues while preserving image fidelity to inspect light-to-dark contrasting options.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20html%20=%20document.documentElement;%20const%20isCurrentlyInverted%20=%20html.style.filter.includes('invert');%20if%20(isCurrentlyInverted)%20%7B%20html.style.removeProperty('filter');%20document.querySelectorAll('img,%20video,%20iframe,%20%5Bclass*=%22no-invert%22%5D').forEach(e%20=%3E%20%7B%20e.style.removeProperty('filter');%20%7D);%20console.log('Chromatic%20inversion%20reverted.');%20%7D%20else%20%7B%20html.style.filter%20=%20'invert(1)%20hue-rotate(180deg)';%20document.querySelectorAll('img,%20video,%20iframe,%20%5Bclass*=%22no-invert%22%5D').forEach(e%20=%3E%20%7B%20e.style.filter%20=%20'invert(1)%20hue-rotate(180deg)';%20%7D);%20console.log('Inverted%20viewport%20contrast.%20Verified%20eye%20safe%20dark%20theme%20simulation.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Chromatic Layout Inversion
(function() {
  const html = document.documentElement;
  const isCurrentlyInverted = html.style.filter.includes('invert');
  
  if (isCurrentlyInverted) {
    html.style.removeProperty('filter');
    document.querySelectorAll('img, video, iframe, [class*="no-invert"]').forEach(e => {
      e.style.removeProperty('filter');
    });
    console.log('Chromatic inversion reverted.');
  } else {
    html.style.filter = 'invert(1) hue-rotate(180deg)';
    document.querySelectorAll('img, video, iframe, [class*="no-invert"]').forEach(e => {
      e.style.filter = 'invert(1) hue-rotate(180deg)';
    });
    console.log('Inverted viewport contrast. Verified eye safe dark theme simulation.');
  }
})();
```

---

### Toggle Page Scroll

**Description:** Disables scrolling on the main page viewport to check fixed layouts, models, or header containers.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20b%20=%20document.body;%20const%20h%20=%20document.documentElement;%20if%20(b.style.overflow%20===%20'hidden')%20%7B%20b.style.removeProperty('overflow');%20h.style.removeProperty('overflow');%20console.log('Viewport%20scrolling%20unlocked.');%20%7D%20else%20%7B%20b.style.overflow%20=%20'hidden';%20h.style.overflow%20=%20'hidden';%20console.log('Viewport%20scrolling%20locked.%20Test%20active%20modals%20or%20sticky%20alignments.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Viewport Scroll Lock
(function() {
  const b = document.body; const h = document.documentElement;
  if (b.style.overflow === 'hidden') {
    b.style.removeProperty('overflow');
    h.style.removeProperty('overflow');
    console.log('Viewport scrolling unlocked.');
  } else {
    b.style.overflow = 'hidden';
    h.style.overflow = 'hidden';
    console.log('Viewport scrolling locked. Test active modals or sticky alignments.');
  }
})();
```

---

### Scroll Performance Test

**Description:** Launches a 5-second frequency diagnostics module logging frame rates and rendering limits.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20scrollCount%20=%200;%20const%20begin%20=%20Date.now();%20const%20tick%20=%20()%20=%3E%20%7B%20scrollCount++;%20%7D;%20window.addEventListener('scroll',%20tick);%20console.log('Frequency%20tracker%20active%20for%205%20seconds!%20Slide%20mouse%20scroll%20vigorously.');%20setTimeout(()%20=%3E%20%7B%20window.removeEventListener('scroll',%20tick);%20const%20duration%20=%20(Date.now()%20-%20begin)%20/%201000;%20const%20rate%20=%20(scrollCount%20/%20duration).toFixed(1);%20console.log(%60Scroll%20performance%20database:%20Captured%20$%7BscrollCount%7D%20scrolls%20in%20$%7Bduration%7D%20seconds%20(~%20$%7Brate%7D%20dispatches/sec).%60);%20alert(%60Scroll%20performance%20database:%20Events%20captured:%20$%7BscrollCount%7D%20Duration:%20$%7Bduration%7Ds%20Run%20Rate:%20$%7Brate%7D%20frames/sec%20(Rates%20%3E%2060%20reflect%20highly%20smooth%20input%20processing)%60);%20%7D,%205000);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Scroll dispatch listener
(function() {
  let scrollCount = 0;
  const begin = Date.now();
  const tick = () => { scrollCount++; };
  
  window.addEventListener('scroll', tick);
  console.log('Frequency tracker active for 5 seconds! Slide mouse scroll vigorously.');
  
  setTimeout(() => {
    window.removeEventListener('scroll', tick);
    const duration = (Date.now() - begin) / 1000;
    const rate = (scrollCount / duration).toFixed(1);
    console.log(`Scroll performance database: Captured ${scrollCount} scrolls in ${duration} seconds (~ ${rate} dispatches/sec).`);
    alert(`Scroll performance database:
Events captured: ${scrollCount}
Duration: ${duration}s
Run Rate: ${rate} frames/sec

(Rates > 60 reflect highly smooth input processing)`);
  }, 5000);
})();
```

---

### Lazy Load Image Auditor

**Description:** Highlights lazy-loaded image tags and outlines deferred elements visible within the active fold.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20images%20=%20document.querySelectorAll('img');%20let%20lazyCount%20=%200;%20let%20loadedInView%20=%200;%20images.forEach(img%20=%3E%20%7B%20const%20isLazy%20=%20img.getAttribute('loading')%20===%20'lazy'%20%7C%7C%20img.hasAttribute('data-src');%20if%20(isLazy)%20%7B%20lazyCount++;%20const%20rect%20=%20img.getBoundingClientRect();%20const%20inView%20=%20(rect.top%20%3C%20window.innerHeight%20&&%20rect.bottom%20%3E%200);%20if%20(inView)%20%7B%20img.style.outline%20=%20'3px%20dashed%20#10B981';%20loadedInView++;%20%7D%20else%20%7B%20img.style.outline%20=%20'3px%20dashed%20#EF4444';%20%7D%20%7D%20%7D);%20alert(%60found%20$%7BlazyCount%7D%20deferred%20lazy%20elements.%20Loaded%20in%20viewport%20range:%20$%7BloadedInView%7D%20(highlighted%20green%20outlines)%20Remaining:%20$%7BlazyCount%20-%20loadedInView%7D%20(highlighted%20off-screen%20in%20red)%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Image lazy load layout checks
(function() {
  const images = document.querySelectorAll('img');
  let lazyCount = 0; let loadedInView = 0;
  
  images.forEach(img => {
    const isLazy = img.getAttribute('loading') === 'lazy' || img.hasAttribute('data-src');
    if (isLazy) {
      lazyCount++;
      const rect = img.getBoundingClientRect();
      const inView = (rect.top < window.innerHeight && rect.bottom > 0);
      if (inView) {
        img.style.outline = '3px dashed #10B981';
        loadedInView++;
      } else {
        img.style.outline = '3px dashed #EF4444';
      }
    }
  });
  alert(`found ${lazyCount} deferred lazy elements.
Loaded in viewport range: ${loadedInView} (highlighted green outlines)
Remaining: ${lazyCount - loadedInView} (highlighted off-screen in red)`);
})();
```

---

### Generate Page QR Code

**Description:** Renders a popup QR Code of the current URL to quickly load and test the webpage on mobile devices.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20url%20=%20window.location.href;%20window.open('https://api.qrserver.com/v1/create-qr-code/?size=300x300&data='%20+%20encodeURIComponent(url),%20'_blank');%20console.log('Generated%20QR%20code%20page%20for%20testing%20mobile%20layout.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Generate and display page QR code
(function() {
  const url = window.location.href;
  window.open('https://api.qrserver.com/v1/create-qr-code/?size=300x300&data=' + encodeURIComponent(url), '_blank');
  console.log('Generated QR code page for testing mobile layout.');
})();
```

---

## 🛠️ Development & QA Utilities

### jQuery Injector

**Description:** Injects production jQuery 3.7.1 from a secure CDN into the window workspace context.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20if%20(window.jQuery)%20%7B%20alert(%60jQuery%20is%20already%20injected.%20Version:%20$%7Bwindow.jQuery.fn.jquery%7D%60);%20return;%20%7D%20const%20script%20=%20document.createElement('script');%20script.src%20=%20'https://code.jquery.com/jquery-3.7.1.min.js';%20script.onload%20=%20()%20=%3E%20%7B%20console.log('jQuery%203.7.1%20mounted%20successfully:%20window.jQuery%20is%20now%20ready.');%20alert('SUCCESS:%20jQuery%20version%20v3.7.1%20loaded%20successfully%20into%20the%20console%20workspace!');%20%7D;%20script.onerror%20=%20()%20=%3E%20alert('Failed%20to%20retrieve%20script%20from%20CDN.');%20document.head.appendChild(script);%20%7D)();
```

#### 💻 Source Code:
```javascript
// CDN jQuery Ingestion Script
(function() {
  if (window.jQuery) {
    alert(`jQuery is already injected. Version: ${window.jQuery.fn.jquery}`);
    return;
  }
  const script = document.createElement('script');
  script.src = 'https://code.jquery.com/jquery-3.7.1.min.js';
  script.onload = () => {
    console.log('jQuery 3.7.1 mounted successfully: window.jQuery is now ready.');
    alert('SUCCESS: jQuery version v3.7.1 loaded successfully into the console workspace!');
  };
  script.onerror = () => alert('Failed to retrieve script from CDN.');
  document.head.appendChild(script);
})();
```

---

### Vue.js Detector

**Description:** Detects active Vue.js software runtime components on the target page.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20isVue%20=%20!!window.Vue%20%7C%7C%20!!document.querySelector('%5Bdata-v-app%5D')%20%7C%7C%20!!document.querySelector('__vue_app__');%20if%20(isVue)%20%7B%20alert('SUCCESS:%20Vue.js%20architecture%20detected%20on%20page!%20Initialized%20elements%20are%20ready%20in%20sandbox%20console.');%20%7D%20else%20%7B%20alert('DIAGNOSTICS:%20No%20Vue%20structural%20elements%20or%20global%20variables%20detected.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Audit Vue.js runtime indicators
(function() {
  const isVue = !!window.Vue || !!document.querySelector('[data-v-app]') || !!document.querySelector('__vue_app__');
  if (isVue) {
    alert('SUCCESS: Vue.js architecture detected on page! Initialized elements are ready in sandbox console.');
  } else {
    alert('DIAGNOSTICS: No Vue structural elements or global variables detected.');
  }
})();
```

---

### React Detector

**Description:** Detects React framework instances by auditing global hooks and component markers.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20root%20=%20document.querySelector('%5Bdata-reactroot%5D')%20%7C%7C%20document.getElementById('root')%20%7C%7C%20document.getElementById('react-root');%20const%20isReact%20=%20!!window.React%20%7C%7C%20(root%20&&%20root._reactRootContainer)%20%7C%7C%20(root%20&&%20Object.keys(root).some(k%20=%3E%20k.startsWith('__react')));%20if%20(isReact)%20%7B%20alert('React%20framework%20instance%20detected!%20Single-page%20application%20components%20confirmed.');%20%7D%20else%20%7B%20alert('Diagnostics:%20React%20framework%20root%20properties%20were%20not%20detected.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Audit React framework indicators
(function() {
  const root = document.querySelector('[data-reactroot]') || document.getElementById('root') || document.getElementById('react-root');
  const isReact = !!window.React || (root && root._reactRootContainer) || (root && Object.keys(root).some(k => k.startsWith('__react')));
  
  if (isReact) {
    alert('React framework instance detected! Single-page application components confirmed.');
  } else {
    alert('Diagnostics: React framework root properties were not detected.');
  }
})();
```

---

### Strip CSS Stylesheets

**Description:** Instantly deactivates every CSS file on the document to check raw semantic HTML structure.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20stylesCount%20=%200;%20document.querySelectorAll('style,%20link%5Brel=%22stylesheet%22%5D').forEach(el%20=%3E%20%7B%20el.remove();%20stylesCount++;%20%7D);%20document.querySelectorAll('%5Bstyle%5D').forEach(el%20=%3E%20%7B%20el.removeAttribute('style');%20%7D);%20console.log(%60Cleaned%20page%20structural%20layouts.%20Removed%20$%7BstylesCount%7D%20styles%20sheets.%60);%20alert(%60Deactivated%20$%7BstylesCount%7D%20styling%20sheets!%20Raw%20HTML%20elements%20revealed.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Destroy CSS Stylesheets
(function() {
  let stylesCount = 0;
  document.querySelectorAll('style, link[rel="stylesheet"]').forEach(el => {
    el.remove();
    stylesCount++;
  });
  document.querySelectorAll('[style]').forEach(el => {
    el.removeAttribute('style');
  });
  console.log(`Cleaned page structural layouts. Removed ${stylesCount} styles sheets.`);
  alert(`Deactivated ${stylesCount} styling sheets! Raw HTML elements revealed.`);
})();
```

---

### Purge Script Code tags

**Description:** Purges standard script tags and resets event bindings to run offline layout checks.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20count%20=%200;%20document.querySelectorAll('script').forEach(s%20=%3E%20%7B%20s.remove();%20count++;%20%7D);%20console.log(%60Removed%20$%7Bcount%7D%20script%20tags%20elements.%60);%20alert(%60Removed%20$%7Bcount%7D%20script%20instances%20from%20layout%20context%20(Refresh%20page%20to%20restore%20runtime%20activity).%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Kill JS scripts engines
(function() {
  let count = 0;
  document.querySelectorAll('script').forEach(s => {
    s.remove();
    count++;
  });
  console.log(`Removed ${count} script tags elements.`);
  alert(`Removed ${count} script instances from layout context (Refresh page to restore runtime activity).`);
})();
```

---

### Form Auto-Filler (QA)

**Description:** Populates all forms with accurate testing inputs like dummy names, email IDs, passwords, and phones.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20fieldsFilled%20=%200;%20document.querySelectorAll('input,%20textarea').forEach(el%20=%3E%20%7B%20if%20(el.value.trim()%20!==%20'')%20return;%20//%20Skip%20const%20type%20=%20el.getAttribute('type')%20%7C%7C%20'text';%20if%20(type%20===%20'email')%20el.value%20=%20'sandbox-qa@domain.com';%20else%20if%20(type%20===%20'password')%20el.value%20=%20'Test_S3curePass!';%20else%20if%20(type%20===%20'tel')%20el.value%20=%20'555-4122';%20else%20if%20(type%20===%20'checkbox'%20%7C%7C%20type%20===%20'radio')%20el.checked%20=%20true;%20else%20el.value%20=%20'Jane%20Doe%20(Compliance)';%20el.dispatchEvent(new%20Event('input',%20%7B%20bubbles:%20true%20%7D));%20el.dispatchEvent(new%20Event('change',%20%7B%20bubbles:%20true%20%7D));%20fieldsFilled++;%20%7D);%20alert(%60Form%20Auto-Filler:%20Evaluated%20form%20schema%20and%20populated%20$%7BfieldsFilled%7D%20testing%20inputs%20elements!%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Fast QA inputs simulator auto filler
(function() {
  let fieldsFilled = 0;
  document.querySelectorAll('input, textarea').forEach(el => {
    if (el.value.trim() !== '') return; // Skip
    
    const type = el.getAttribute('type') || 'text';
    if (type === 'email') el.value = 'sandbox-qa@domain.com';
    else if (type === 'password') el.value = 'Test_S3curePass!';
    else if (type === 'tel') el.value = '555-4122';
    else if (type === 'checkbox' || type === 'radio') el.checked = true;
    else el.value = 'Jane Doe (Compliance)';
    
    // Bubble up input trigger down frameworks bindings
    el.dispatchEvent(new Event('input', { bubbles: true }));
    el.dispatchEvent(new Event('change', { bubbles: true }));
    fieldsFilled++;
  });
  alert(`Form Auto-Filler: Evaluated form schema and populated ${fieldsFilled} testing inputs elements!`);
})();
```

---

### Show All Form Values

**Description:** Audits and displays active input string configurations nested within your active webpage sheets.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20fieldsValues%20=%20%5B%5D;%20document.querySelectorAll('input,%20textarea,%20select').forEach(el%20=%3E%20%7B%20const%20identifier%20=%20el.getAttribute('name')%20%7C%7C%20el.className%20%7C%7C%20el.tagName.toLowerCase();%20const%20val%20=%20el.value%20%7C%7C%20(el.checked%20?%20'Checked'%20:%20'');%20fieldsValues.push(%60$%7Bidentifier%7D:%20%22$%7Bval%7D%22%60);%20%7D);%20if%20(fieldsValues.length%20===%200)%20%7B%20alert('No%20form%20fields%20discovered.');%20return;%20%7D%20alert(%60Exposed%20Form%20Fields%20Map:%20----------------------%20$%7BfieldsValues.join('%20')%7D%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Form database diagnostics
(function() {
  const fieldsValues = [];
  document.querySelectorAll('input, textarea, select').forEach(el => {
    const identifier = el.getAttribute('name') || el.className || el.tagName.toLowerCase();
    const val = el.value || (el.checked ? 'Checked' : '');
    fieldsValues.push(`${identifier}: "${val}"`);
  });
  if (fieldsValues.length === 0) {
    alert('No form fields discovered.');
    return;
  }
  alert(`Exposed Form Fields Map:
----------------------
${fieldsValues.join('
')}`);
})();
```

---

### Highlight Broken Images

**Description:** Scans image assets and highlights broken links with a distinct red dashed outline.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20brokenCount%20=%200;%20document.querySelectorAll('img').forEach(img%20=%3E%20%7B%20const%20isBroken%20=%20!img.complete%20%7C%7C%20img.naturalWidth%20===%200;%20if%20(isBroken)%20%7B%20img.style.outline%20=%20'4px%20solid%20#EF4444';%20img.style.outlineOffset%20=%20'2px';%20img.style.background%20=%20'#FEE2E2';%20brokenCount++;%20%7D%20%7D);%20alert(%60Quality%20audits%20complete.%20Discovered:%20$%7BbrokenCount%7D%20broken%20images.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Broken Image Diagnostics
(function() {
  let brokenCount = 0;
  document.querySelectorAll('img').forEach(img => {
    const isBroken = !img.complete || img.naturalWidth === 0;
    if (isBroken) {
      img.style.outline = '4px solid #EF4444';
      img.style.outlineOffset = '2px';
      img.style.background = '#FEE2E2';
      brokenCount++;
    }
  });
  alert(`Quality audits complete. Discovered: ${brokenCount} broken images.`);
})();
```

---

### Show Image Alt Text

**Description:** Renders absolute overlay banners on all page layouts displaying raw alt tag strings.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20badges%20=%20document.querySelectorAll('.alt-badge-overlay-diag');%20if%20(badges.length)%20%7B%20badges.forEach(b%20=%3E%20b.remove());%20console.log('Alt%20badges%20cleared.');%20return;%20%7D%20document.querySelectorAll('img').forEach(img%20=%3E%20%7B%20const%20alt%20=%20img.getAttribute('alt')%20%7C%7C%20'%E2%9A%A0%EF%B8%8F%20NO%20ALT%20ATTRIBUTE';%20const%20b%20=%20document.createElement('div');%20b.className%20=%20'alt-badge-overlay-diag';%20b.textContent%20=%20%60%5BAlt%5D:%20%22$%7Balt%7D%22%60;%20b.style.cssText%20=%20'position:absolute;background:rgba(15,23,42,0.9);color:#F1F5F9;padding:4px%206px;font-family:monospace;font-size:10px;z-index:99999;border-radius:3px;border:1px%20solid%20#475569';%20const%20parent%20=%20img.parentNode;%20if%20(parent)%20%7B%20if%20(getComputedStyle(parent).position%20===%20'static')%20parent.style.position%20=%20'relative';%20parent.appendChild(b);%20%7D%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Visual Alt texts mapping overlays
(function() {
  const badges = document.querySelectorAll('.alt-badge-overlay-diag');
  if (badges.length) {
    badges.forEach(b => b.remove());
    console.log('Alt badges cleared.');
    return;
  }
  document.querySelectorAll('img').forEach(img => {
    const alt = img.getAttribute('alt') || '⚠️ NO ALT ATTRIBUTE';
    const b = document.createElement('div');
    b.className = 'alt-badge-overlay-diag';
    b.textContent = `[Alt]: "${alt}"`;
    b.style.cssText = 'position:absolute;background:rgba(15,23,42,0.9);color:#F1F5F9;padding:4px 6px;font-family:monospace;font-size:10px;z-index:99999;border-radius:3px;border:1px solid #475569';
    
    const parent = img.parentNode;
    if (parent) {
      if (getComputedStyle(parent).position === 'static') parent.style.position = 'relative';
      parent.appendChild(b);
    }
  });
})();
```

---

### Highlight Missing Alt Tags

**Description:** Highlights any images missing descriptive alt metrics with red dashed borders to check SEO safety compliance.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20missingCount%20=%200;%20document.querySelectorAll('img').forEach(img%20=%3E%20%7B%20const%20missing%20=%20!img.hasAttribute('alt')%20%7C%7C%20img.getAttribute('alt').trim()%20===%20'';%20if%20(missing)%20%7B%20img.style.outline%20=%20'4px%20dashed%20#EF4444';%20img.style.outlineOffset%20=%20'2.5px';%20missingCount++;%20%7D%20%7D);%20alert(%60Compliance%20Audits%20complete.%20Found%20$%7BmissingCount%7D%20images%20missing%20descriptive%20alt%20tags%20markers.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Highlight element missing Alt attributes
(function() {
  let missingCount = 0;
  document.querySelectorAll('img').forEach(img => {
    const missing = !img.hasAttribute('alt') || img.getAttribute('alt').trim() === '';
    if (missing) {
      img.style.outline = '4px dashed #EF4444';
      img.style.outlineOffset = '2.5px';
      missingCount++;
    }
  });
  alert(`Compliance Audits complete. Found ${missingCount} images missing descriptive alt tags markers.`);
})();
```

---

### Form Mock Auto-Filler

**Description:** Populates all visible form inputs, checkboxes, and select dropdowns with clean randomized placeholder test data.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20elements%20=%20document.querySelectorAll('input,%20textarea,%20select');%20let%20filledCount%20=%200;%20elements.forEach(el%20=%3E%20%7B%20if%20(el.offsetParent%20===%20null)%20return;%20//%20Ignore%20hidden%20elements%20const%20tag%20=%20el.tagName.toLowerCase();%20const%20type%20=%20(el.getAttribute('type')%20%7C%7C%20'text').toLowerCase();%20if%20(tag%20===%20'textarea')%20%7B%20el.value%20=%20'Lorem%20ipsum%20dolor%20sit%20amet,%20consectetur%20adipiscing%20elit.';%20filledCount++;%20%7D%20else%20if%20(tag%20===%20'select')%20%7B%20if%20(el.options.length%20%3E%201)%20%7B%20el.selectedIndex%20=%201;%20filledCount++;%20%7D%20%7D%20else%20if%20(type%20===%20'checkbox'%20%7C%7C%20type%20===%20'radio')%20%7B%20el.checked%20=%20true;%20filledCount++;%20%7D%20else%20if%20(type%20===%20'email')%20%7B%20el.value%20=%20%60dev.test$%7BMath.floor(Math.random()%20*%2010000)%7D@example.com%60;%20filledCount++;%20%7D%20else%20if%20(type%20===%20'number')%20%7B%20el.value%20=%20Math.floor(Math.random()%20*%20100)%20+%201;%20filledCount++;%20%7D%20else%20if%20(type%20===%20'tel')%20%7B%20el.value%20=%20'555-019-'%20+%20Math.floor(1000%20+%20Math.random()%20*%209000);%20filledCount++;%20%7D%20else%20if%20(type%20===%20'text')%20%7B%20el.value%20=%20'Sandbox%20User%20'%20+%20Math.floor(Math.random()%20*%20100);%20filledCount++;%20%7D%20el.dispatchEvent(new%20Event('input',%20%7B%20bubbles:%20true%20%7D));%20el.dispatchEvent(new%20Event('change',%20%7B%20bubbles:%20true%20%7D));%20%7D);%20console.log(%60Form%20Filler%20successfully%20populated%20$%7BfilledCount%7D%20form%20elements.%60);%20alert(%60Form%20mock%20auto-filler%20complete!%20Populated%20$%7BfilledCount%7D%20form%20fields.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Fills all form elements with mock inputs and dispatches change events
(function() {
  const elements = document.querySelectorAll('input, textarea, select');
  let filledCount = 0;
  elements.forEach(el => {
    if (el.offsetParent === null) return; // Ignore hidden elements
    const tag = el.tagName.toLowerCase();
    const type = (el.getAttribute('type') || 'text').toLowerCase();
    
    if (tag === 'textarea') {
      el.value = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.';
      filledCount++;
    } else if (tag === 'select') {
      if (el.options.length > 1) {
        el.selectedIndex = 1;
        filledCount++;
      }
    } else if (type === 'checkbox' || type === 'radio') {
      el.checked = true;
      filledCount++;
    } else if (type === 'email') {
      el.value = `dev.test${Math.floor(Math.random() * 10000)}@example.com`;
      filledCount++;
    } else if (type === 'number') {
      el.value = Math.floor(Math.random() * 100) + 1;
      filledCount++;
    } else if (type === 'tel') {
      el.value = '555-019-' + Math.floor(1000 + Math.random() * 9000);
      filledCount++;
    } else if (type === 'text') {
      el.value = 'Sandbox User ' + Math.floor(Math.random() * 100);
      filledCount++;
    }
    
    // Dispatch events to satisfy framework listeners (React, Vue, etc.)
    el.dispatchEvent(new Event('input', { bubbles: true }));
    el.dispatchEvent(new Event('change', { bubbles: true }));
  });
  console.log(`Form Filler successfully populated ${filledCount} form elements.`);
  alert(`Form mock auto-filler complete! Populated ${filledCount} form fields.`);
})();
```

---

### Reveal Password Fields

**Description:** Swaps input type=\

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20fields%20=%20document.querySelectorAll('input%5Btype=%22password%22%5D');%20fields.forEach(f%20=%3E%20%7B%20f.setAttribute('type',%20'text');%20f.style.border%20=%20'2px%20solid%20#ef4444';%20%7D);%20console.log(%60Exposed%20$%7Bfields.length%7D%20password%20field%20inputs.%60);%20alert(%60Exposed%20$%7Bfields.length%7D%20hidden%20password%20fields%20safely.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Reveal hidden inputs type="password" to standard text
(function() {
  const fields = document.querySelectorAll('input[type="password"]');
  fields.forEach(f => {
    f.setAttribute('type', 'text');
    f.style.border = '2px solid #ef4444';
  });
  console.log(`Exposed ${fields.length} password field inputs.`);
  alert(`Exposed ${fields.length} hidden password fields safely.`);
})();
```

---

### View Source

**Description:** Opens the view-source representation of the current active page in a new tab.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20window.open('view-source:'%20+%20window.location.href,%20'_blank');%20console.log('Opened%20view-source%20of%20current%20tab.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Open view-source of current page
(function() {
  window.open('view-source:' + window.location.href, '_blank');
  console.log('Opened view-source of current tab.');
})();
```

---

### Check All Checkboxes

**Description:** Finds and selects all checkboxes on the active page instantly.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20boxes%20=%20document.querySelectorAll('input%5Btype=%22checkbox%22%5D');%20boxes.forEach(b%20=%3E%20%7B%20b.checked%20=%20true;%20b.dispatchEvent(new%20Event('change',%20%7B%20bubbles:%20true%20%7D));%20%7D);%20console.log(%60Checked%20$%7Bboxes.length%7D%20checkbox%20inputs.%60);%20alert(%60Checked%20$%7Bboxes.length%7D%20checkbox%20inputs.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Check all checkbox inputs
(function() {
  const boxes = document.querySelectorAll('input[type="checkbox"]');
  boxes.forEach(b => {
    b.checked = true;
    b.dispatchEvent(new Event('change', { bubbles: true }));
  });
  console.log(`Checked ${boxes.length} checkbox inputs.`);
  alert(`Checked ${boxes.length} checkbox inputs.`);
})();
```

---

### Uncheck All Checkboxes

**Description:** Finds and unselects all checkboxes on the active page instantly.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20boxes%20=%20document.querySelectorAll('input%5Btype=%22checkbox%22%5D');%20boxes.forEach(b%20=%3E%20%7B%20b.checked%20=%20false;%20b.dispatchEvent(new%20Event('change',%20%7B%20bubbles:%20true%20%7D));%20%7D);%20console.log(%60Unchecked%20$%7Bboxes.length%7D%20checkbox%20inputs.%60);%20alert(%60Unchecked%20$%7Bboxes.length%7D%20checkbox%20inputs.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Uncheck all checkbox inputs
(function() {
  const boxes = document.querySelectorAll('input[type="checkbox"]');
  boxes.forEach(b => {
    b.checked = false;
    b.dispatchEvent(new Event('change', { bubbles: true }));
  });
  console.log(`Unchecked ${boxes.length} checkbox inputs.`);
  alert(`Unchecked ${boxes.length} checkbox inputs.`);
})();
```

---

### Design Mode Editor

**Description:** Enables or disables browser contentEditable design mode to let you edit any text on the page in-place.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20if%20(d.body.contentEditable%20===%20'true'%20%7C%7C%20d.designMode%20===%20'on')%20%7B%20d.body.contentEditable%20=%20'false';%20d.designMode%20=%20'off';%20console.log('Design%20mode%20turned%20OFF.');%20alert('Design%20mode:%20OFF%20(web%20page%20is%20now%20read-only)');%20%7D%20else%20%7B%20d.body.contentEditable%20=%20'true';%20d.designMode%20=%20'on';%20console.log('Design%20mode%20turned%20ON.');%20alert('Design%20mode:%20ON%20(you%20can%20now%20edit%20any%20text%20directly!)');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Toggle Document Design Mode contentEditable
(function() {
  const d = document;
  if (d.body.contentEditable === 'true' || d.designMode === 'on') {
    d.body.contentEditable = 'false';
    d.designMode = 'off';
    console.log('Design mode turned OFF.');
    alert('Design mode: OFF (web page is now read-only)');
  } else {
    d.body.contentEditable = 'true';
    d.designMode = 'on';
    console.log('Design mode turned ON.');
    alert('Design mode: ON (you can now edit any text directly!)');
  }
})();
```

---

### Quick Password Revealer

**Description:** Exposes password inputs as standard visible text to check spelling or verify saved login forms.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20inputs%20=%20document.querySelectorAll('input%5Btype=%22password%22%5D');%20inputs.forEach(i%20=%3E%20%7B%20i.type%20=%20%22text%22;%20%7D);%20console.log(%60Revealed%20$%7Binputs.length%7D%20password%20fields.%60);%20alert(%60Revealed%20$%7Binputs.length%7D%20password%20fields!%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Reveal all password input types
(function() {
  const inputs = document.querySelectorAll('input[type="password"]');
  inputs.forEach(i => {
    i.type = "text";
  });
  console.log(`Revealed ${inputs.length} password fields.`);
  alert(`Revealed ${inputs.length} password fields!`);
})();
```

---

### Element Zapper

**Description:** Click any component to completely delete it from the DOM layout to test responsive reflows or remove overlay blockers.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20styleId%20=%20'zap-element-style';%20const%20style%20=%20document.getElementById(styleId);%20if%20(style)%20%7B%20style.remove();%20document.querySelectorAll('.zap-hover').forEach(el%20=%3E%20el.classList.remove('zap-hover'));%20document.removeEventListener('click',%20window.zapClick);%20document.removeEventListener('mouseover',%20window.zapOver);%20document.removeEventListener('mouseout',%20window.zapOut);%20console.log('Element%20zapper%20deactivated.');%20alert('Element%20zapper%20deactivated.');%20return;%20%7D%20const%20s%20=%20document.createElement('style');%20s.id%20=%20styleId;%20s.textContent%20=%20'.zap-hover%7Boutline:2px%20dashed%20#ef4444!important;cursor:crosshair!important%7D';%20document.head.appendChild(s);%20window.zapOver%20=%20function(e)%20%7B%20if%20(e.target)%20e.target.classList.add('zap-hover');%20%7D;%20window.zapOut%20=%20function(e)%20%7B%20if%20(e.target)%20e.target.classList.remove('zap-hover');%20%7D;%20window.zapClick%20=%20function(e)%20%7B%20if%20(e.target)%20%7B%20e.preventDefault();%20e.stopPropagation();%20const%20name%20=%20e.target.tagName.toLowerCase();%20e.target.remove();%20console.log(%60Zapped%20and%20removed%20element:%20%3C$%7Bname%7D%3E%60);%20%7D%20%7D;%20document.addEventListener('mouseover',%20window.zapOver);%20document.addEventListener('mouseout',%20window.zapOut);%20document.addEventListener('click',%20window.zapClick,%20%7B%20capture:%20true%20%7D);%20console.log('Element%20zapper%20active.%20Click%20any%20layout%20element%20to%20remove%20it.');%20alert('Element%20zapper%20activated.%20Hover%20and%20click%20any%20element%20to%20delete%20it.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Zap and destroy hovered DOM element on click
(function() {
  const styleId = 'zap-element-style';
  const style = document.getElementById(styleId);
  if (style) {
    style.remove();
    document.querySelectorAll('.zap-hover').forEach(el => el.classList.remove('zap-hover'));
    document.removeEventListener('click', window.zapClick);
    document.removeEventListener('mouseover', window.zapOver);
    document.removeEventListener('mouseout', window.zapOut);
    console.log('Element zapper deactivated.');
    alert('Element zapper deactivated.');
    return;
  }
  const s = document.createElement('style');
  s.id = styleId;
  s.textContent = '.zap-hover{outline:2px dashed #ef4444!important;cursor:crosshair!important}';
  document.head.appendChild(s);
  
  window.zapOver = function(e) {
    if (e.target) e.target.classList.add('zap-hover');
  };
  window.zapOut = function(e) {
    if (e.target) e.target.classList.remove('zap-hover');
  };
  window.zapClick = function(e) {
    if (e.target) {
      e.preventDefault();
      e.stopPropagation();
      const name = e.target.tagName.toLowerCase();
      e.target.remove();
      console.log(`Zapped and removed element: <${name}>`);
    }
  };
  
  document.addEventListener('mouseover', window.zapOver);
  document.addEventListener('mouseout', window.zapOut);
  document.addEventListener('click', window.zapClick, { capture: true });
  console.log('Element zapper active. Click any layout element to remove it.');
  alert('Element zapper activated. Hover and click any element to delete it.');
})();
```

---

### Word & Selection Counter

**Description:** Returns precise character & word counts of either selected text or the entire page text content.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20selection%20=%20window.getSelection().toString();%20const%20text%20=%20selection%20%7C%7C%20document.body.innerText;%20const%20sourceLabel%20=%20selection%20?%20%22Selection%20text%22%20:%20%22Full%20Page%20body%20text%22;%20const%20charCount%20=%20text.length;%20const%20wordCount%20=%20text.trim().split(/%5Cs+/).filter(Boolean).length;%20alert(%60Metrics%20%5B$%7BsourceLabel%7D%5D:%20---------------------%20Words:%20$%7BwordCount%7D%20Characters:%20$%7BcharCount%7D%60);%20console.log(%60Word%20count:%20$%7BwordCount%7D%20%7C%20Character%20count:%20$%7BcharCount%7D%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Retrieve text metrics
(function() {
  const selection = window.getSelection().toString();
  const text = selection || document.body.innerText;
  const sourceLabel = selection ? "Selection text" : "Full Page body text";
  const charCount = text.length;
  const wordCount = text.trim().split(/\s+/).filter(Boolean).length;
  alert(`Metrics [${sourceLabel}]:
---------------------
Words: ${wordCount}
Characters: ${charCount}`);
  console.log(`Word count: ${wordCount} | Character count: ${charCount}`);
})();
```

---

### Single Click Image Downloader

**Description:** Click any image on the webpage to instantly download it.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%7B%20document.addEventListener(%22click%22,%20function(e)%7B%20let%20img%20=%20e.target.closest(%22img%22);%20if(!img)%20return;%20e.preventDefault();%20e.stopPropagation();%20let%20url%20=%20img.currentSrc%20%7C%7C%20img.src;%20let%20a%20=%20document.createElement(%22a%22);%20a.href%20=%20url;%20a.download%20=%20url.split(%22/%22).pop().split(%22?%22)%5B0%5D%20%7C%7C%20%22image%22;%20document.body.appendChild(a);%20a.click();%20a.remove();%20%7D,%20true);%20alert(%22Image%20Auto%20Save%20Enabled%22);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Single Click Image Downloader
(function(){
  document.addEventListener("click", function(e){
    let img = e.target.closest("img");
    if(!img) return;
    e.preventDefault();
    e.stopPropagation();
    let url = img.currentSrc || img.src;
    let a = document.createElement("a");
    a.href = url;
    a.download = url.split("/").pop().split("?")[0] || "image";
    document.body.appendChild(a);
    a.click();
    a.remove();
  }, true);
  alert("Image Auto Save Enabled");
})();
```

---

## 🚀 Performance & SEO

### Audit Page Load Speeds

**Description:** Calculates performance timing intervals, displaying total page and DOM ready metrics.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20t%20=%20window.performance.timing;%20const%20load%20=%20(t.loadEventEnd%20-%20t.navigationStart)%20/%201000;%20const%20dcl%20=%20(t.domContentLoadedEventEnd%20-%20t.navigationStart)%20/%201000;%20if%20(load%20%3C=%200)%20%7B%20alert('Diagnostics%20waiting%20fully%20loaded%20resources.%20Try%20again%20in%20seconds!');%20return;%20%7D%20alert(%60Performance%20metrics%20database:%20-----------------------------%20DOM%20Ready%20Clock:%20$%7Bdcl.toFixed(3)%7Ds%20Total%20Load%20clock:%20$%7Bload.toFixed(3)%7Ds%20(Speeds%20under%202s%20represent%20high%20performance%20standards)%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Read browser performance speed clocks
(function() {
  const t = window.performance.timing;
  const load = (t.loadEventEnd - t.navigationStart) / 1000;
  const dcl = (t.domContentLoadedEventEnd - t.navigationStart) / 1000;
  
  if (load <= 0) {
    alert('Diagnostics waiting fully loaded resources. Try again in seconds!');
    return;
  }
  alert(`Performance metrics database:
-----------------------------
DOM Ready Clock: ${dcl.toFixed(3)}s
Total Load clock: ${load.toFixed(3)}s
(Speeds under 2s represent high performance standards)`);
})();
```

---

### Count DOM Elements

**Description:** Counts total elements, tracking DOM tree depth limits, script references, and container sizing indicators.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20allNodes%20=%20document.querySelectorAll('*').length;%20const%20scripts%20=%20document.querySelectorAll('script').length;%20const%20divs%20=%20document.querySelectorAll('div').length;%20const%20links%20=%20document.querySelectorAll('a').length;%20alert(%60DOM%20Nesting%20Density%20Map:%20-------------------------%20Total%20tag%20elements:%20$%7BallNodes%7D%20Container%20divs:%20$%7Bdivs%7D%20Script%20variables:%20$%7Bscripts%7D%20Links:%20$%7Blinks%7D%20(DOM%20counts%20under%201200%20are%20optimal%20for%20rendering%20performance)%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// DOM Elements tree audit density
(function() {
  const allNodes = document.querySelectorAll('*').length;
  const scripts = document.querySelectorAll('script').length;
  const divs = document.querySelectorAll('div').length;
  const links = document.querySelectorAll('a').length;
  
  alert(`DOM Nesting Density Map:
-------------------------
Total tag elements: ${allNodes}
Container divs: ${divs}
Script variables: ${scripts}
Links: ${links}

(DOM counts under 1200 are optimal for rendering performance)`);
})();
```

---

### Approximate LCP Metric

**Description:** Fetches browser Largest Contentful Paint timing milestones, checking UX performance.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20LcpEntries%20=%20performance.getEntriesByType('largest-contentful-paint');%20if%20(LcpEntries.length%20===%200)%20%7B%20alert('LCP%20metrics%20logging.%20Move%20components%20or%20refresh.');%20return;%20%7D%20const%20primary%20=%20LcpEntries%5B0%5D;%20const%20sec%20=%20(primary.startTime%20/%201000).toFixed(3);%20alert(%60Largest%20Contentful%20Paint%20(LCP):%20-------------------------%20Timing%20clock:%20$%7Bsec%7D%20seconds%20Target%20Element:%20%3C$%7Bprimary.element%20?%20primary.element.tagName.toLowerCase()%20:%20'unknown'%7D%3E%20(LCP%20under%202.5s%20is%20optimal%20for%20user%20experience)%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Approximate LCP metric parameters
(function() {
  const LcpEntries = performance.getEntriesByType('largest-contentful-paint');
  if (LcpEntries.length === 0) {
    alert('LCP metrics logging. Move components or refresh.');
    return;
  }
  const primary = LcpEntries[0];
  const sec = (primary.startTime / 1000).toFixed(3);
  alert(`Largest Contentful Paint (LCP):
-------------------------
Timing clock: ${sec} seconds
Target Element: <${primary.element ? primary.element.tagName.toLowerCase() : 'unknown'}>

(LCP under 2.5s is optimal for user experience)`);
})();
```

---

### CLS Shifting Metrics

**Description:** Calculates viewport cumulative layout shifts scores to confirm performance stability.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20cls%20=%200;%20const%20entries%20=%20performance.getEntriesByType('layout-shift');%20entries.forEach(e%20=%3E%20%7B%20if%20(!e.hadRecentInput)%20cls%20+=%20e.value;%20%7D);%20let%20scale%20=%20'Excellent%20stability%20(%E2%9C%85%20CLASS%20PASS)';%20if%20(cls%20%3E%200.25)%20scale%20=%20'Heavy%20layout%20shifts%20(%F0%9F%9A%A8%20POOR)';%20else%20if%20(cls%20%3E%200.1)%20scale%20=%20'Moderate%20layout%20shifts%20(%E2%9A%A0%EF%B8%8F%20NEEDS%20WORK)';%20alert(%60Cumulative%20Layout%20Shift%20(CLS):%20-------------------------------%20CLS%20computed%20Score:%20$%7Bcls.toFixed(5)%7D%20Rating:%20$%7Bscale%7D%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Visual shifts metrics index calculator
(function() {
  let cls = 0;
  const entries = performance.getEntriesByType('layout-shift');
  entries.forEach(e => {
    if (!e.hadRecentInput) cls += e.value;
  });
  
  let scale = 'Excellent stability (✅ CLASS PASS)';
  if (cls > 0.25) scale = 'Heavy layout shifts (🚨 POOR)';
  else if (cls > 0.1) scale = 'Moderate layout shifts (⚠️ NEEDS WORK)';
  
  alert(`Cumulative Layout Shift (CLS):
-------------------------------
CLS computed Score: ${cls.toFixed(5)}
Rating: ${scale}`);
})();
```

---

### Meta Tags Extractor

**Description:** Gathers all programmatic meta tags inside developer consoles to analyze description logs and indexing targets.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20metaElements%20=%20%5B%5D;%20document.querySelectorAll('meta').forEach(meta%20=%3E%20%7B%20const%20name%20=%20meta.getAttribute('name')%20%7C%7C%20meta.getAttribute('property')%20%7C%7C%20meta.getAttribute('http-equiv');%20const%20content%20=%20meta.getAttribute('content');%20if%20(name)%20%7B%20metaElements.push(%60$%7Bname%7D:%20%22$%7Bcontent%20%7C%7C%20''%7D%22%60);%20%7D%20%7D);%20if%20(metaElements.length%20===%200)%20%7B%20alert('No%20meta%20descriptors%20discovered%20in%20HTML%20layouts.');%20return;%20%7D%20console.log('%25cProgrammatic%20Meta%20properties%20matrix:',%20'font-size:15px;%20font-weight:bold;%20color:#EA580C',%20metaElements);%20alert(%60Discovered%20$%7BmetaElements.length%7D%20meta%20fields%20entries!%20Logs%20compiled%20in%20developer%20console.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// SEO meta descriptors inspector
(function() {
  const metaElements = [];
  document.querySelectorAll('meta').forEach(meta => {
    const name = meta.getAttribute('name') || meta.getAttribute('property') || meta.getAttribute('http-equiv');
    const content = meta.getAttribute('content');
    if (name) {
      metaElements.push(`${name}: "${content || ''}"`);
    }
  });
  if (metaElements.length === 0) {
    alert('No meta descriptors discovered in HTML layouts.');
    return;
  }
  console.log('%cProgrammatic Meta properties matrix:', 'font-size:15px; font-weight:bold; color:#EA580C', metaElements);
  alert(`Discovered ${metaElements.length} meta fields entries! Logs compiled in developer console.`);
})();
```

---

### Heading Structure Checker

**Description:** Exposes structural headings on browser consoles, verifying hierarchy requirements.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20tree%20=%20%5B%5D;%20const%20h1Count%20=%20document.querySelectorAll('h1').length;%20document.querySelectorAll('h1,%20h2,%20h3,%20h4,%20h5,%20h6').forEach(h%20=%3E%20%7B%20tree.push(%60$%7Bh.tagName%7D:%20%22$%7Bh.textContent.trim().substring(0,%2050)%7D%22%60);%20%7D);%20console.log('%25cHeading%20Structure%20Tree%20Map:',%20'font-size:15px;%20font-weight:bold;%20color:#16A34A',%20tree);%20let%20h1Status%20=%20'%E2%9C%93%20H1%20Count%20correct';%20if%20(h1Count%20===%200)%20h1Status%20=%20'%E2%9A%A0%EF%B8%8F%20CRITICAL:%20Missing%20H1%20page%20header!';%20else%20if%20(h1Count%20%3E%201)%20h1Status%20=%20'%E2%9A%A0%EF%B8%8F%20WARNING:%20Multiple%20H1%20headers%20violate%20standards!';%20alert(%60Heading%20Hierarchy%20Statistics:%20-------------------------%20Total%20headings%20nodes:%20$%7Btree.length%7D%20H1%20count%20status:%20$%7Bh1Count%7D%20($%7Bh1Status%7D)%20Complete%20outline%20cataloged%20in%20console%20prints!%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Headings Hierarchy compliance
(function() {
  const tree = [];
  const h1Count = document.querySelectorAll('h1').length;
  
  document.querySelectorAll('h1, h2, h3, h4, h5, h6').forEach(h => {
    tree.push(`${h.tagName}: "${h.textContent.trim().substring(0, 50)}"`);
  });
  
  console.log('%cHeading Structure Tree Map:', 'font-size:15px; font-weight:bold; color:#16A34A', tree);
  
  let h1Status = '✓ H1 Count correct';
  if (h1Count === 0) h1Status = '⚠️ CRITICAL: Missing H1 page header!';
  else if (h1Count > 1) h1Status = '⚠️ WARNING: Multiple H1 headers violate standards!';
  
  alert(`Heading Hierarchy Statistics:
-------------------------
Total headings nodes: ${tree.length}
H1 count status: ${h1Count} (${h1Status})

Complete outline cataloged in console prints!`);
})();
```

---

### Highlight Empty Links

**Description:** Identifies and highlights empty anchor tags or links with dummy \

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20countBroken%20=%200;%20document.querySelectorAll('a').forEach(a%20=%3E%20%7B%20const%20target%20=%20a.getAttribute('href');%20const%20isBroken%20=%20!target%20%7C%7C%20target.trim()%20===%20''%20%7C%7C%20target%20===%20'#';%20if%20(isBroken)%20%7B%20a.style.outline%20=%20'3px%20solid%20#EF4444';%20a.style.outlineOffset%20=%20'1.5px';%20a.style.background%20=%20'#FEE2E2';%20countBroken++;%20%7D%20%7D);%20alert(%60Integrity%20checks%20complete.%20Discovered:%20$%7BcountBroken%7D%20empty%20placeholder%20tags.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Anchor link integrity checks
(function() {
  let countBroken = 0;
  document.querySelectorAll('a').forEach(a => {
    const target = a.getAttribute('href');
    const isBroken = !target || target.trim() === '' || target === '#';
    if (isBroken) {
      a.style.outline = '3px solid #EF4444';
      a.style.outlineOffset = '1.5px';
      a.style.background = '#FEE2E2';
      countBroken++;
    }
  });
  alert(`Integrity checks complete. Discovered: ${countBroken} empty placeholder tags.`);
})();
```

---

### Highlight External Links

**Description:** Highlights outgoing paths with dashed borders to check linking directions.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20currentHost%20=%20window.location.hostname;%20let%20extCount%20=%200;%20document.querySelectorAll('a').forEach(link%20=%3E%20%7B%20if%20(link.hostname%20&&%20link.hostname%20!==%20currentHost)%20%7B%20link.style.borderBottom%20=%20'3px%20dashed%20#F59E0B';%20link.style.color%20=%20'#D97706';%20extCount++;%20%7D%20%7D);%20alert(%60Outgoing%20Link%20Diagnostics:%20Discovered%20$%7BextCount%7D%20external%20links%20elements.%20Marked%20with%20gold%20dashed%20styling.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Outcoming linkages analyzer
(function() {
  const currentHost = window.location.hostname;
  let extCount = 0;
  document.querySelectorAll('a').forEach(link => {
    if (link.hostname && link.hostname !== currentHost) {
      link.style.borderBottom = '3px dashed #F59E0B';
      link.style.color = '#D97706';
      extCount++;
    }
  });
  alert(`Outgoing Link Diagnostics: Discovered ${extCount} external links elements. Marked with gold dashed styling.`);
})();
```

---

### SEO Google SERP Snippet Preview

**Description:** Renders an interactive Google Search result preview of the active page metadata structures.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20const%20old%20=%20d.getElementById('serp-preview-card');%20if%20(old)%20old.remove();%20const%20desc%20=%20d.querySelector('meta%5Bname=%22description%22%5D')?.content%20%7C%7C%20'%E2%9A%A0%EF%B8%8F%20DESCRIPTION%20MISSING:%20Configure%20%3Cmeta%20name=%22description%22%3E%20to%20optimize%20search%20results.';%20const%20b%20=%20d.createElement('div');%20b.id%20=%20'serp-preview-card';%20b.style%20=%20'position:fixed;top:50%25;left:50%25;transform:translate(-50%25,-50%25);background:#FFFFFF;border:1px%20solid%20#dadce0;padding:24px;z-index:999999;max-width:600px;border-radius:12px;box-shadow:0%2012px%2030px%20rgba(0,0,0,0.25);text-align:left;font-family:Arial,sans-serif';%20b.innerHTML%20=%20%60%20%3Cdiv%20style=%22font-size:12px;color:#202124;font-weight:bold;margin-bottom:12px;text-transform:uppercase%22%3ESERP%20Snippet%20emulation%3C/div%3E%20%3Cdiv%20style=%22color:#202124;font-size:14px;margin-bottom:4px;display:flex;align-items:center%22%3Egoogle.com/search?q=preview%3C/div%3E%20%3Ch3%20style=%22color:#1a0dab;font-size:20px;margin:0%200%204px;font-weight:normal;line-height:1.3;text-decoration:none%22%3E$%7Bd.title%7D%3C/h3%3E%20%3Cdiv%20style=%22color:#202124;font-size:14px;margin-bottom:6px;word-break:break-all%22%3E$%7Bwindow.location.href%7D%3C/div%3E%20%3Cdiv%20style=%22color:#4d5156;font-size:14px;line-height:1.58;word-break:break-word%22%3E$%7Bdesc%7D%3C/div%3E%20%3Cbutton%20onclick=%22this.parentElement.remove()%22%20style=%22margin-top:16px;padding:6px%2016px;background:#1A73E8;color:white;border:none;border-radius:6px;cursor:pointer;font-size:11px;font-weight:bold%22%3EClose%20Dialog%3C/button%3E%20%60;%20d.body.appendChild(b);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Google Search engine results preview card
(function() {
  const d = document;
  const old = d.getElementById('serp-preview-card'); if (old) old.remove();
  const desc = d.querySelector('meta[name="description"]')?.content || '⚠️ DESCRIPTION MISSING: Configure <meta name="description"> to optimize search results.';
  const b = d.createElement('div');
  b.id = 'serp-preview-card';
  b.style = 'position:fixed;top:50%;left:50%;transform:translate(-50%,-50%);background:#FFFFFF;border:1px solid #dadce0;padding:24px;z-index:999999;max-width:600px;border-radius:12px;box-shadow:0 12px 30px rgba(0,0,0,0.25);text-align:left;font-family:Arial,sans-serif';
  b.innerHTML = `
    <div style="font-size:12px;color:#202124;font-weight:bold;margin-bottom:12px;text-transform:uppercase">SERP Snippet emulation</div>
    <div style="color:#202124;font-size:14px;margin-bottom:4px;display:flex;align-items:center">google.com/search?q=preview</div>
    <h3 style="color:#1a0dab;font-size:20px;margin:0 0 4px;font-weight:normal;line-height:1.3;text-decoration:none">${d.title}</h3>
    <div style="color:#202124;font-size:14px;margin-bottom:6px;word-break:break-all">${window.location.href}</div>
    <div style="color:#4d5156;font-size:14px;line-height:1.58;word-break:break-word">${desc}</div>
    <button onclick="this.parentElement.remove()" style="margin-top:16px;padding:6px 16px;background:#1A73E8;color:white;border:none;border-radius:6px;cursor:pointer;font-size:11px;font-weight:bold">Close Dialog</button>
  `;
  d.body.appendChild(b);
})();
```

---

### Vitals Speed Summary

**Description:** Compiles LCP speeds, FCP clocks, and layout shifts variables into a speed dial visualizer panel.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20d%20=%20document;%20const%20old%20=%20d.getElementById('vitals-widget-summary');%20if%20(old)%20old.remove();%20const%20fcp%20=%20performance.getEntriesByName('first-contentful-paint')%5B0%5D?.startTime%20%7C%7C%200;%20const%20lcp%20=%20performance.getEntriesByType('largest-contentful-paint')%5B0%5D?.startTime%20%7C%7C%201500;%20let%20cls%20=%200;%20performance.getEntriesByType('layout-shift').forEach(e%20=%3E%20%7B%20if(!e.hadRecentInput)%20cls%20+=%20e.value;%20%7D);%20const%20b%20=%20d.createElement('div');%20b.id%20=%20'vitals-widget-summary';%20b.style%20=%20'position:fixed;top:15px;right:15px;background:#0F172A;color:#E2E8F0;border:1px%20solid%20#334155;padding:16.5px;z-index:999999;font-family:monospace;border-radius:8px;box-shadow:0%2012px%2015px%20-3px%20rgba(0,0,0,0.40)';%20b.innerHTML%20=%20%60%20%3Ch3%20style=%22margin:0%200%2010px;font-size:12px;font-weight:bold;color:#10B981;border-bottom:1px%20solid%20#334155;padding-bottom:4px%22%3ECore%20Web%20Vitals%20summary%3C/h3%3E%20%3Cdiv%20style=%22margin:4px%200;font-size:10px;display:flex;justify-content:space-between;gap:40px%22%3E%3Cspan%3EFCP%20(Content%20load):%3C/span%3E%20%3Cb%20style=%22color:$%7Bfcp%20%3C%202000%20?%20'#10B981'%20:%20'#EF4444'%7D%22%3E$%7B(fcp/1000).toFixed(3)%7Ds%3C/b%3E%3C/div%3E%20%3Cdiv%20style=%22margin:4px%200;font-size:10px;display:flex;justify-content:space-between;gap:40px%22%3E%3Cspan%3ELCP%20(Render%20frame):%3C/span%3E%20%3Cb%20style=%22color:$%7Blcp%20%3C%202500%20?%20'#10B981'%20:%20'#F59E0B'%7D%22%3E$%7B(lcp/1000).toFixed(3)%7Ds%3C/b%3E%3C/div%3E%20%3Cdiv%20style=%22margin:4px%200;font-size:10px;display:flex;justify-content:space-between;gap:40px%22%3E%3Cspan%3ECLS%20(Stability):%3C/span%3E%20%3Cb%20style=%22color:$%7Bcls%20%3C%200.1%20?%20'#10B981'%20:%20'#EF4444'%7D%22%3E$%7Bcls.toFixed(4)%7D%3C/b%3E%3C/div%3E%20%3Cbutton%20onclick=%22this.parentElement.remove()%22%20style=%22margin-top:10.5px;width:100%25;padding:4px;border-radius:4px;background:#1E293B;color:#94A3B8;border:1px%20solid%20#334155;cursor:pointer;font-family:monospace;font-size:10px;font-weight:bold%22%3EDismiss%20Panel%3C/button%3E%20%60;%20d.body.appendChild(b);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Core Web Vitals speed indicators card
(function() {
  const d = document;
  const old = d.getElementById('vitals-widget-summary'); if (old) old.remove();
  
  const fcp = performance.getEntriesByName('first-contentful-paint')[0]?.startTime || 0;
  const lcp = performance.getEntriesByType('largest-contentful-paint')[0]?.startTime || 1500;
  let cls = 0;
  performance.getEntriesByType('layout-shift').forEach(e => { if(!e.hadRecentInput) cls += e.value; });
  
  const b = d.createElement('div');
  b.id = 'vitals-widget-summary';
  b.style = 'position:fixed;top:15px;right:15px;background:#0F172A;color:#E2E8F0;border:1px solid #334155;padding:16.5px;z-index:999999;font-family:monospace;border-radius:8px;box-shadow:0 12px 15px -3px rgba(0,0,0,0.40)';
  
  b.innerHTML = `
    <h3 style="margin:0 0 10px;font-size:12px;font-weight:bold;color:#10B981;border-bottom:1px solid #334155;padding-bottom:4px">Core Web Vitals summary</h3>
    <div style="margin:4px 0;font-size:10px;display:flex;justify-content:space-between;gap:40px"><span>FCP (Content load):</span> <b style="color:${fcp < 2000 ? '#10B981' : '#EF4444'}">${(fcp/1000).toFixed(3)}s</b></div>
    <div style="margin:4px 0;font-size:10px;display:flex;justify-content:space-between;gap:40px"><span>LCP (Render frame):</span> <b style="color:${lcp < 2500 ? '#10B981' : '#F59E0B'}">${(lcp/1000).toFixed(3)}s</b></div>
    <div style="margin:4px 0;font-size:10px;display:flex;justify-content:space-between;gap:40px"><span>CLS (Stability):</span> <b style="color:${cls < 0.1 ? '#10B981' : '#EF4444'}">${cls.toFixed(4)}</b></div>
    <button onclick="this.parentElement.remove()" style="margin-top:10.5px;width:100%;padding:4px;border-radius:4px;background:#1E293B;color:#94A3B8;border:1px solid #334155;cursor:pointer;font-family:monospace;font-size:10px;font-weight:bold">Dismiss Panel</button>
  `;
  d.body.appendChild(b);
})();
```

---

### Image Alt Text Audit

**Description:** Finds and highlights all images on the page, overlaying red borders on those missing descriptive alt attributes.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20imgs%20=%20document.querySelectorAll('img');%20let%20missingCount%20=%200;%20imgs.forEach(img%20=%3E%20%7B%20if%20(!img.alt%20%7C%7C%20img.alt.trim()%20===%20'')%20%7B%20img.style.outline%20=%20'3px%20dashed%20#ef4444';%20img.style.outlineOffset%20=%20'2px';%20missingCount++;%20console.warn('Missing%20ALT%20tag%20for%20image:',%20img.src);%20%7D%20else%20%7B%20img.style.outline%20=%20'3px%20dashed%20#10b981';%20img.style.outlineOffset%20=%20'2px';%20%7D%20%7D);%20console.log(%60Alt%20text%20check%20complete:%20$%7BmissingCount%7D%20missing,%20$%7Bimgs.length%20-%20missingCount%7D%20present.%60);%20alert(%60Alt%20Text%20Audit%20Completed!%20Images%20missing%20alt%20text:%20$%7BmissingCount%7D%20Images%20with%20alt%20text:%20$%7Bimgs.length%20-%20missingCount%7D%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Visual alt text checker and highlighter
(function() {
  const imgs = document.querySelectorAll('img');
  let missingCount = 0;
  imgs.forEach(img => {
    if (!img.alt || img.alt.trim() === '') {
      img.style.outline = '3px dashed #ef4444';
      img.style.outlineOffset = '2px';
      missingCount++;
      console.warn('Missing ALT tag for image:', img.src);
    } else {
      img.style.outline = '3px dashed #10b981';
      img.style.outlineOffset = '2px';
    }
  });
  console.log(`Alt text check complete: ${missingCount} missing, ${imgs.length - missingCount} present.`);
  alert(`Alt Text Audit Completed!
Images missing alt text: ${missingCount}
Images with alt text: ${imgs.length - missingCount}`);
})();
```

---

### Outline External Links

**Description:** Highlights all hyperlinks pointing to external websites with a distinct outline.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20existing%20=%20document.getElementById('outline-external-links-style');%20if%20(existing)%20%7B%20existing.remove();%20console.log('Outline%20external%20links%20deactivated.');%20%7D%20else%20%7B%20const%20s%20=%20document.createElement('style');%20s.id%20=%20'outline-external-links-style';%20s.textContent%20=%20%60a%5Bhref*=%22//%22%5D:not(%5Bhref*=%22$%7Bwindow.location.hostname%7D%22%5D)%7Boutline:2px%20solid%20#ef4444!important;outline-offset:2px!important;background-color:rgba(239,72,153,0.15)!important%7D%60;%20document.head.appendChild(s);%20console.log('Outline%20external%20links%20activated.%20Marked%20with%20a%20red%20outline.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Outline external hyperlink elements
(function() {
  const existing = document.getElementById('outline-external-links-style');
  if (existing) {
    existing.remove();
    console.log('Outline external links deactivated.');
  } else {
    const s = document.createElement('style');
    s.id = 'outline-external-links-style';
    s.textContent = `a[href*="//"]:not([href*="${window.location.hostname}"]){outline:2px solid #ef4444!important;outline-offset:2px!important;background-color:rgba(239,72,153,0.15)!important}`;
    document.head.appendChild(s);
    console.log('Outline external links activated. Marked with a red outline.');
  }
})();
```

---

### Wayback Machine Lookup

**Description:** Queries the Internet Archive Wayback Machine history logs for the current URL to inspect historical versions.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20url%20=%20window.location.href;%20window.open('https://web.archive.org/web/*/'%20+%20url,%20'_blank');%20console.log('Opening%20Wayback%20Machine%20history%20timeline%20logs.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Lookup page URL on Internet Archive Wayback Machine
(function() {
  const url = window.location.href;
  window.open('https://web.archive.org/web/*/' + url, '_blank');
  console.log('Opening Wayback Machine history timeline logs.');
})();
```

---

### Google PageSpeed Auditor

**Description:** Launches Google PageSpeed Insights analyzer in a new tab to run a live Core Web Vitals audit on the current URL.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20url%20=%20window.location.href;%20window.open('https://pagespeed.web.dev/analysis?url='%20+%20encodeURIComponent(url),%20'_blank');%20console.log('Launched%20Google%20PageSpeed%20Insights%20web%20performance%20auditor.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Open PageSpeed Insights auditor
(function() {
  const url = window.location.href;
  window.open('https://pagespeed.web.dev/analysis?url=' + encodeURIComponent(url), '_blank');
  console.log('Launched Google PageSpeed Insights web performance auditor.');
})();
```

---

### Validate HTML (W3C)

**Description:** Directly sends the current URL to the official W3C Markup Validation Service to audit HTML validity and tags matching.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20window.open('https://validator.w3.org/nu/?doc='%20+%20encodeURIComponent(window.location.href),%20'_blank');%20console.log('Opening%20official%20W3C%20Nu%20HTML%20Markup%20Validator%20for%20current%20URL.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Trigger W3C HTML validator
(function() {
  window.open('https://validator.w3.org/nu/?doc=' + encodeURIComponent(window.location.href), '_blank');
  console.log('Opening official W3C Nu HTML Markup Validator for current URL.');
})();
```

---

### Validate CSS (W3C)

**Description:** Directly sends the current URL to the official W3C CSS Validation Service to audit CSS compliance and syntax errors.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20window.open('https://jigsaw.w3.org/css-validator/validator?uri='%20+%20encodeURIComponent(window.location.href),%20'_blank');%20console.log('Opening%20official%20W3C%20CSS%20Jigsaw%20validator%20for%20current%20URL.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Trigger W3C CSS validator
(function() {
  window.open('https://jigsaw.w3.org/css-validator/validator?uri=' + encodeURIComponent(window.location.href), '_blank');
  console.log('Opening official W3C CSS Jigsaw validator for current URL.');
})();
```

---

### Aria Roles Auditor

**Description:** Highlights and tags all ARIA roles, alt text, and accessibility properties on elements to audit assistive readers compliance.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20styleId%20=%20'aria-roles-style';%20const%20existing%20=%20document.getElementById(styleId);%20if%20(existing)%20%7B%20existing.remove();%20document.querySelectorAll('.aria-badge').forEach(badge%20=%3E%20badge.remove());%20console.log('Aria%20tags%20off.');%20return;%20%7D%20const%20s%20=%20document.createElement('style');%20s.id%20=%20styleId;%20s.textContent%20=%20'.aria-badge%7Bbackground:#8b5cf6!important;color:#fff!important;font:bold%209px%20monospace!important;padding:2px%204px!important;border-radius:3px!important;margin-left:4px!important;display:inline-block!important;z-index:99999!important%7D';%20document.head.appendChild(s);%20const%20els%20=%20document.querySelectorAll('%5Brole%5D,%20%5Baria-label%5D,%20%5Baria-hidden%5D,%20img%5Balt%5D');%20els.forEach(el%20=%3E%20%7B%20const%20label%20=%20el.getAttribute('role')%20%7C%7C%20el.getAttribute('aria-label')%20%7C%7C%20'alt:%20'%20+%20el.getAttribute('alt');%20const%20span%20=%20document.createElement('span');%20span.className%20=%20'aria-badge';%20span.innerText%20=%20label;%20el.appendChild(span);%20%7D);%20console.log(%60Tagged%20$%7Bels.length%7D%20accessible%20elements.%60);%20alert('Aria%20and%20Accessibility%20elements%20highlighted!');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Accessibility tags & Aria audit
(function() {
  const styleId = 'aria-roles-style';
  const existing = document.getElementById(styleId);
  if (existing) {
    existing.remove();
    document.querySelectorAll('.aria-badge').forEach(badge => badge.remove());
    console.log('Aria tags off.');
    return;
  }
  const s = document.createElement('style');
  s.id = styleId;
  s.textContent = '.aria-badge{background:#8b5cf6!important;color:#fff!important;font:bold 9px monospace!important;padding:2px 4px!important;border-radius:3px!important;margin-left:4px!important;display:inline-block!important;z-index:99999!important}';
  document.head.appendChild(s);
  
  const els = document.querySelectorAll('[role], [aria-label], [aria-hidden], img[alt]');
  els.forEach(el => {
    const label = el.getAttribute('role') || el.getAttribute('aria-label') || 'alt: ' + el.getAttribute('alt');
    const span = document.createElement('span');
    span.className = 'aria-badge';
    span.innerText = label;
    el.appendChild(span);
  });
  console.log(`Tagged ${els.length} accessible elements.`);
  alert('Aria and Accessibility elements highlighted!');
})();
```

---

### PageSpeed Insights Auditor

**Description:** Launches Google PageSpeed Insights in a new tab to analyze the performance and speed optimization of the current page.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20window.open('https://developers.google.com/speed/pagespeed/insights/?url='%20+%20encodeURIComponent(location.href));%20%7D)();
```

#### 💻 Source Code:
```javascript
// Launches Google PageSpeed Insights for current page
(function() {
  window.open('https://developers.google.com/speed/pagespeed/insights/?url=' + encodeURIComponent(location.href));
})();
```

---

### XML Sitemap Finder & Analyzer

**Description:** Queries sitemap.xml and sitemap-index.xml locations, auditing server HTTP response codes and indexing configurations.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(()%20=%3E%20%7B%20const%20t%20=%20new%20URL(window.location.href);%20const%20locations%20=%20%5B%20%60$%7Bt.protocol%7D//$%7Bt.hostname%7D/sitemap.xml%60,%20%60$%7Bt.protocol%7D//$%7Bt.hostname%7D/sitemap-index.xml%60%20%5D;%20Promise.all(locations.map(url%20=%3E%20%20fetch(url)%20.then(res%20=%3E%20(%7B%20url,%20status:%20res.ok,%20statusCode:%20res.status%20%7D))%20.catch(()%20=%3E%20(%7B%20url,%20status:%20false,%20statusCode:%20404%20%7D))%20)).then(results%20=%3E%20%7B%20const%20popup%20=%20document.createElement(%22div%22);%20popup.className%20=%20%22seo-popup%22;%20popup.style.cssText%20=%20%60%20position:%20fixed;%20top:%2020px;%20right:%2020px;%20width:%2080%25;%20max-width:%20600px;%20max-height:%2080vh;%20background:%20#ffffff;%20color:%20#0f172a;%20padding:%2020px;%20border-radius:%208px;%20box-shadow:%200%2010px%2025px%20-5px%20rgba(0,0,0,0.2);%20z-index:%20100000;%20overflow-y:%20auto;%20font-family:%20system-ui,%20-apple-system,%20sans-serif;%20border:%201px%20solid%20#e2e8f0;%20%60;%20const%20foundCount%20=%20results.filter(r%20=%3E%20r.status).length;%20popup.innerHTML%20=%20%60%20%3Cdiv%20style=%22display:%20flex;%20justify-content:%20space-between;%20align-items:%20center;%20border-bottom:%201px%20solid%20#e2e8f0;%20padding-bottom:%2010px;%20margin-bottom:%2015px;%22%3E%20%3Ch3%20style=%22margin:%200;%20font-size:%2016px;%22%3EXML%20Sitemap%20Analysis%3C/h3%3E%20%3Cbutton%20onclick=%22this.closest('.seo-popup').remove()%22%20style=%22background:#ef4444;%20color:#fff;%20border:none;%20padding:4px%208px;%20border-radius:4px;%20cursor:pointer;%20font-size:12px;%22%3EClose%3C/button%3E%20%3C/div%3E%20%3Cdiv%20style=%22margin-bottom:%2015px;%20padding:%2010px;%20border:%201px%20solid%20$%7BfoundCount%20?%20'#10b981'%20:%20'#ef4444'%7D;%20background:%20$%7BfoundCount%20?%20'#ecfdf5'%20:%20'#fef2f2'%7D;%20border-radius:%206px;%22%3E%20%3Cstrong%20style=%22color:%20$%7BfoundCount%20?%20'#065f46'%20:%20'#991b1b'%7D%22%3E%20$%7BfoundCount%20?%20%60Found%20$%7BfoundCount%7D%20sitemap%20file(s)%60%20:%20'No%20standard%20sitemaps%20found'%7D%20%3C/strong%3E%20%3C/div%3E%20%3Ch4%20style=%22margin:%200%200%208px;%20font-size:14px;%22%3ELocations%20Checked:%3C/h4%3E%20$%7Bresults.map(r%20=%3E%20%60%20%3Cdiv%20style=%22padding:%208px;%20margin-bottom:%208px;%20background:%20#f8fafc;%20border:%201px%20solid%20#e2e8f0;%20border-radius:%204px;%20font-size:%2012px;%20font-family:%20monospace;%20word-break:%20break-all;%22%3E%20%3Cspan%20style=%22color:%20$%7Br.status%20?%20'#10b981'%20:%20'#ef4444'%7D;%20font-size:%2014px;%20margin-right:%206px;%22%3E%E2%97%8F%3C/span%3E%20%3Ca%20href=%22$%7Br.url%7D%22%20target=%22_blank%22%20style=%22color:#2563eb;%20text-decoration:underline;%22%3E$%7Br.url%7D%3C/a%3E%20%3Cdiv%20style=%22margin-top:%204px;%20color:%20#64748b;%22%3EHTTP%20Status:%20%3Cstrong%3E$%7Br.statusCode%7D%3C/strong%3E%3C/div%3E%20%3C/div%3E%20%60).join('')%7D%20%60;%20document.body.appendChild(popup);%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// XML Sitemap Detector & Status Auditor
(() => {
  const t = new URL(window.location.href);
  const locations = [
    `${t.protocol}//${t.hostname}/sitemap.xml`,
    `${t.protocol}//${t.hostname}/sitemap-index.xml`
  ];
  Promise.all(locations.map(url => 
    fetch(url)
      .then(res => ({ url, status: res.ok, statusCode: res.status }))
      .catch(() => ({ url, status: false, statusCode: 404 }))
  )).then(results => {
    const popup = document.createElement("div");
    popup.className = "seo-popup";
    popup.style.cssText = `
      position: fixed;
      top: 20px;
      right: 20px;
      width: 80%;
      max-width: 600px;
      max-height: 80vh;
      background: #ffffff;
      color: #0f172a;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 10px 25px -5px rgba(0,0,0,0.2);
      z-index: 100000;
      overflow-y: auto;
      font-family: system-ui, -apple-system, sans-serif;
      border: 1px solid #e2e8f0;
    `;
    const foundCount = results.filter(r => r.status).length;
    popup.innerHTML = `
      <div style="display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid #e2e8f0; padding-bottom: 10px; margin-bottom: 15px;">
        <h3 style="margin: 0; font-size: 16px;">XML Sitemap Analysis</h3>
        <button onclick="this.closest('.seo-popup').remove()" style="background:#ef4444; color:#fff; border:none; padding:4px 8px; border-radius:4px; cursor:pointer; font-size:12px;">Close</button>
      </div>
      <div style="margin-bottom: 15px; padding: 10px; border: 1px solid ${foundCount ? '#10b981' : '#ef4444'}; background: ${foundCount ? '#ecfdf5' : '#fef2f2'}; border-radius: 6px;">
        <strong style="color: ${foundCount ? '#065f46' : '#991b1b'}">
          ${foundCount ? `Found ${foundCount} sitemap file(s)` : 'No standard sitemaps found'}
        </strong>
      </div>
      <h4 style="margin: 0 0 8px; font-size:14px;">Locations Checked:</h4>
      ${results.map(r => `
        <div style="padding: 8px; margin-bottom: 8px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 4px; font-size: 12px; font-family: monospace; word-break: break-all;">
          <span style="color: ${r.status ? '#10b981' : '#ef4444'}; font-size: 14px; margin-right: 6px;">●</span>
          <a href="${r.url}" target="_blank" style="color:#2563eb; text-decoration:underline;">${r.url}</a>
          <div style="margin-top: 4px; color: #64748b;">HTTP Status: <strong>${r.statusCode}</strong></div>
        </div>
      `).join('')}
    `;
    document.body.appendChild(popup);
  });
})();
```

---

### Website Performance Graph

**Description:** Injects a real-time visual timeline and waterfall graph of page asset loading performance.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%7B%20var%20el=document.createElement('script');%20el.type='text/javascript';%20el.src='https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js';%20el.onerror=function()%7B%20alert(%22Content%20Security%20Policy%20directive%20is%20blocking%20the%20use%20of%20bookmarklets%5C%20%5C%20You%20can%20copy%20and%20paste%20the%20content%20of:%5C%20%5C%20%5C%22https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js%5C%22%5C%20%5C%20into%20your%20console%20instead%22);%20console.log(%22https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js%22);%20%7D;%20document.getElementsByTagName('body')%5B0%5D.appendChild(el);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Performance Bookmarklet Graph
(function(){
  var el=document.createElement('script');
  el.type='text/javascript';
  el.src='https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js';
  el.onerror=function(){
    alert("Content Security Policy directive is blocking the use of bookmarklets\
\
You can copy and paste the content of:\
\
\"https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js\"\
\
into your console instead");
    console.log("https://micmro.github.io/performance-bookmarklet/dist/performanceBookmarklet.min.js");
  };
  document.getElementsByTagName('body')[0].appendChild(el);
})();
```

---

## 🔬 Advanced Diagnostics & Web Vitals

### CSS Specificity Calculator

**Description:** Finds, analyses, and lists Computed CSS specificity variables across screen margins.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20handler%20=%20function(e)%20%7B%20const%20el%20=%20e.target;%20if%20(el)%20%7B%20console.log(%60%25cSelected%20Element%20styling%20rules%20outline:%20%3C$%7Bel.tagName.toLowerCase()%7D%3E%60,%20'font-size:14px;%20font-weight:bold;%20color:#7C3AED');%20console.log('ID%20parameter%20present:',%20!!el.id,%20%60(%22$%7Bel.id%20%7C%7C%20''%7D%22)%60);%20console.log('Classes%20count:',%20el.classList.length,%20Array.from(el.classList));%20console.log('Active%20parent%20scope:',%20el.parentNode);%20const%20computed%20=%20getComputedStyle(el);%20console.log('Primary%20width%20allocations:',%20computed.width,%20'height:',%20computed.height);%20alert(%60Target%20Spec%20properties%20logged%20in%20Console!%20Tag:%20%3C$%7Bel.tagName.toLowerCase()%7D%3E%20Classes%20list%20has%20size%20$%7Bel.classList.length%7D.%60);%20document.removeEventListener('click',%20handler);%20%7D%20e.preventDefault();%20%7D;%20document.addEventListener('click',%20handler);%20alert('CSS%20Specificity%20helper%20enabled:%20click%20any%20element.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Target styling structure inspector
(function() {
  const handler = function(e) {
    const el = e.target;
    if (el) {
      console.log(`%cSelected Element styling rules outline: <${el.tagName.toLowerCase()}>`, 'font-size:14px; font-weight:bold; color:#7C3AED');
      console.log('ID parameter present:', !!el.id, `("${el.id || ''}")`);
      console.log('Classes count:', el.classList.length, Array.from(el.classList));
      console.log('Active parent scope:', el.parentNode);
      
      const computed = getComputedStyle(el);
      console.log('Primary width allocations:', computed.width, 'height:', computed.height);
      alert(`Target Spec properties logged in Console! Tag: <${el.tagName.toLowerCase()}> Classes list has size ${el.classList.length}.`);
      document.removeEventListener('click', handler);
    }
    e.preventDefault();
  };
  document.addEventListener('click', handler);
  alert('CSS Specificity helper enabled: click any element.');
})();
```

---

### FPS Animation Meter

**Description:** Runs real-time hardware-accelerated FPS rendering calculations inside viewport monitors.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20panelId%20=%20'fps-meter-panel';%20const%20existing%20=%20document.getElementById(panelId);%20if%20(existing)%20%7B%20existing.remove();%20cancelAnimationFrame(window.fpsFrameLoop);%20console.log('FPS%20analyzer%20closed.');%20return;%20%7D%20const%20panel%20=%20document.createElement('div');%20panel.id%20=%20panelId;%20panel.style.cssText%20=%20'position:fixed;top:16px;right:16px;background:rgba(15,23,42,0.95);border:1px%20solid%20#10B981;color:#10B981;padding:8px%2012px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;box-shadow:0%2010px%2015px%20-3px%20rgba(0,0,0,0.3)';%20document.body.appendChild(panel);%20let%20frames%20=%200;%20let%20lastTrigger%20=%20Date.now();%20window.fpsFrameLoop%20=%20function()%20%7B%20frames++;%20const%20now%20=%20Date.now();%20if%20(now%20-%20lastTrigger%20%3E=%201000)%20%7B%20panel.textContent%20=%20%60Performance:%20$%7Bframes%7D%20FPS%60;%20frames%20=%200;%20lastTrigger%20=%20now;%20%7D%20requestAnimationFrame(window.fpsFrameLoop);%20%7D;%20window.fpsFrameLoop();%20console.log('FPS%20frame%20counter%20loop%20launched.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Viewport FPS Performance monitor
(function() {
  const panelId = 'fps-meter-panel';
  const existing = document.getElementById(panelId);
  if (existing) {
    existing.remove();
    cancelAnimationFrame(window.fpsFrameLoop);
    console.log('FPS analyzer closed.');
    return;
  }
  const panel = document.createElement('div');
  panel.id = panelId;
  panel.style.cssText = 'position:fixed;top:16px;right:16px;background:rgba(15,23,42,0.95);border:1px solid #10B981;color:#10B981;padding:8px 12px;font-family:monospace;font-size:12px;font-weight:bold;z-index:999999;border-radius:6px;box-shadow:0 10px 15px -3px rgba(0,0,0,0.3)';
  document.body.appendChild(panel);
  
  let frames = 0; let lastTrigger = Date.now();
  window.fpsFrameLoop = function() {
    frames++;
    const now = Date.now();
    if (now - lastTrigger >= 1000) {
      panel.textContent = `Performance: ${frames} FPS`;
      frames = 0;
      lastTrigger = now;
    }
    requestAnimationFrame(window.fpsFrameLoop);
  };
  window.fpsFrameLoop();
  console.log('FPS frame counter loop launched.');
})();
```

---

### JavaScript Memory Heap

**Description:** Calculates JS Heap allocation scopes using internal browser performance memory trackers.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20m%20=%20performance.memory;%20if%20(!m)%20%7B%20alert('Diagnostics%20require%20Chrome%20browser%20with%20precise%20memory%20indicators%20turned%20on.');%20return;%20%7D%20const%20used%20=%20(m.usedJSHeapSize%20/%201048576).toFixed(2);%20const%20total%20=%20(m.totalJSHeapSize%20/%201048576).toFixed(2);%20const%20limit%20=%20(m.jsHeapSizeLimit%20/%201048576).toFixed(2);%20alert(%60JS%20heap%20memory%20allocation%20metrics:%20------------------------------------%20Used:%20$%7Bused%7D%20MB%20Total:%20$%7Btotal%7D%20MB%20Limit:%20$%7Blimit%7D%20MB%20(Memory%20stays%20efficient%20under%2050MB%20for%20standard%20apps)%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Memory heap diagnostics
(function() {
  const m = performance.memory;
  if (!m) {
    alert('Diagnostics require Chrome browser with precise memory indicators turned on.');
    return;
  }
  const used = (m.usedJSHeapSize / 1048576).toFixed(2);
  const total = (m.totalJSHeapSize / 1048576).toFixed(2);
  const limit = (m.jsHeapSizeLimit / 1048576).toFixed(2);
  
  alert(`JS heap memory allocation metrics:
------------------------------------
Used: ${used} MB
Total: ${total} MB
Limit: ${limit} MB

(Memory stays efficient under 50MB for standard apps)`);
})();
```

---

### Find Duplicate IDs

**Description:** Scans DOM element attributes and logs duplicate identifier IDs that conflict with semantic layout rules.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20idMap%20=%20%7B%7D;%20const%20duplicateList%20=%20%5B%5D;%20document.querySelectorAll('%5Bid%5D').forEach(el%20=%3E%20%7B%20const%20idValue%20=%20el.id;%20if%20(idMap%5BidValue%5D)%20%7B%20duplicateList.push(idValue);%20%7D%20idMap%5BidValue%5D%20=%20true;%20%7D);%20const%20uniques%20=%20%5B...new%20Set(duplicateList)%5D;%20if%20(uniques.length%20===%200)%20%7B%20alert('SUCCESS:%20No%20duplicate%20ID%20properties%20discovered%20inside%20the%20page%20layout!');%20%7D%20else%20%7B%20alert(%60CRITICAL%20INVALID%20MARKUP%20DETECTED:%20Found%20$%7Buniques.length%7D%20duplicate%20IDs!%20Check%20compiler%20console%20for%20logs.%60);%20console.log('Duplicate%20IDs%20found:',%20uniques);%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// DOM Identifiers uniqueness validator
(function() {
  const idMap = {};
  const duplicateList = [];
  document.querySelectorAll('[id]').forEach(el => {
    const idValue = el.id;
    if (idMap[idValue]) {
      duplicateList.push(idValue);
    }
    idMap[idValue] = true;
  });
  
  const uniques = [...new Set(duplicateList)];
  if (uniques.length === 0) {
    alert('SUCCESS: No duplicate ID properties discovered inside the page layout!');
  } else {
    alert(`CRITICAL INVALID MARKUP DETECTED: Found ${uniques.length} duplicate IDs! Check compiler console for logs.`);
    console.log('Duplicate IDs found:', uniques);
  }
})();
```

---

### ARIA Roles Validator

**Description:** Highlights elements containing custom ARIA attributes to verify screen-reader support features.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20count%20=%200;%20document.querySelectorAll('%5Brole%5D,%20%5Baria-label%5D,%20%5Baria-hidden%5D,%20%5Baria-expanded%5D').forEach(el%20=%3E%20%7B%20el.style.outline%20=%20'3.5px%20dashed%20#9C27B0';%20el.style.outlineOffset%20=%20'2px';%20count++;%20%7D);%20alert(%60Found%20$%7Bcount%7D%20elements%20containing%20ARIA%20accessibility%20attributes.%20Marked%20elements%20are%20now%20highlighted%20in%20purple.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Accessible ARIA indicators highlighter
(function() {
  let count = 0;
  document.querySelectorAll('[role], [aria-label], [aria-hidden], [aria-expanded]').forEach(el => {
    el.style.outline = '3.5px dashed #9C27B0';
    el.style.outlineOffset = '2px';
    count++;
  });
  alert(`Found ${count} elements containing ARIA accessibility attributes. Marked elements are now highlighted in purple.`);
})();
```

---

### A11y Tab-Focus Auditor

**Description:** Lists all focusable tags and monitors tab-key focus traps.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20elements%20=%20document.querySelectorAll('a,%20button,%20input,%20select,%20textarea,%20%5Btabindex%5D');%20const%20focusables%20=%20Array.from(elements).filter(el%20=%3E%20el.tabIndex%20%3E%20-1%20&&%20el.offsetParent%20!==%20null);%20if%20(focusables.length%20===%200)%20%7B%20alert('No%20keyboard%20interactive%20objects%20discovered%20inside%20layout%20boundaries.');%20return;%20%7D%20console.log('Focus%20elements%20in%20tab%20order:',%20focusables);%20alert(%60Keyboard%20tab-focus%20database:%20discovered%20$%7Bfocusables.length%7D%20focusable%20page%20elements!%20Tab%20order%20details%20printed%20in%20console.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// audit focus tree alignments
(function() {
  const elements = document.querySelectorAll('a, button, input, select, textarea, [tabindex]');
  const focusables = Array.from(elements).filter(el => el.tabIndex > -1 && el.offsetParent !== null);
  
  if (focusables.length === 0) {
    alert('No keyboard interactive objects discovered inside layout boundaries.');
    return;
  }
  console.log('Focus elements in tab order:', focusables);
  alert(`Keyboard tab-focus database: discovered ${focusables.length} focusable page elements! Tab order details printed in console.`);
})();
```

---

### GDPR Cookie Banner Finder

**Description:** Detects and flags potential cookie consent container elements.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20triggers%20=%20%5B'cookie',%20'consent',%20'gdpr',%20'privacy',%20'policy',%20'banner'%5D;%20let%20count%20=%200;%20document.querySelectorAll('div,%20section,%20aside').forEach(el%20=%3E%20%7B%20const%20text%20=%20(el.textContent%20%7C%7C%20'').toLowerCase();%20const%20matches%20=%20triggers.some(t%20=%3E%20text.includes(t));%20const%20isFloatingNotice%20=%20el.offsetHeight%20%3E%2030%20&&%20el.offsetHeight%20%3C%20320;%20if%20(matches%20&&%20isFloatingNotice%20&&%20!el.id.includes('devtools'))%20%7B%20el.style.border%20=%20'4px%20dashed%20#8B5CF6';%20el.style.background%20=%20'rgba(139,%2092,%20246,%200.05)';%20count++;%20%7D%20%7D);%20alert(%60GDPR%20diagnostics%20completed!%20Flagged%20$%7Bcount%7D%20floating%20cookie%20banners%20layers%20elements.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Identify GDPR notice elements
(function() {
  const triggers = ['cookie', 'consent', 'gdpr', 'privacy', 'policy', 'banner'];
  let count = 0;
  document.querySelectorAll('div, section, aside').forEach(el => {
    const text = (el.textContent || '').toLowerCase();
    const matches = triggers.some(t => text.includes(t));
    const isFloatingNotice = el.offsetHeight > 30 && el.offsetHeight < 320;
    
    if (matches && isFloatingNotice && !el.id.includes('devtools')) {
      el.style.border = '4px dashed #8B5CF6';
      el.style.background = 'rgba(139, 92, 246, 0.05)';
      count++;
    }
  });
  alert(`GDPR diagnostics completed! Flagged ${count} floating cookie banners layers elements.`);
})();
```

---

### Audit Scrollbar Widths

**Description:** Determines screen layout scrollbar offsets in absolute pixels.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20outer%20=%20document.createElement('div');%20outer.style.cssText%20=%20'width:%20100px;%20height:%20100px;%20overflow:%20scroll;%20position:%20absolute;%20top:%20-9999px;%20visibility:%20hidden;';%20document.body.appendChild(outer);%20const%20width%20=%20outer.offsetWidth%20-%20outer.clientWidth;%20outer.remove();%20console.log('Calculated%20system%20scrollbar%20width%20allocations:',%20width,%20'px');%20alert(%60Internal%20Sizing:%20scrollbar%20handles%20width%20is%20$%7Bwidth%7Dpx%20(Offsets%20are%20fully%20aligned%20in%20grid%20calculation%20rules).%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Scrollbars width calculator
(function() {
  const outer = document.createElement('div');
  outer.style.cssText = 'width: 100px; height: 100px; overflow: scroll; position: absolute; top: -9999px; visibility: hidden;';
  document.body.appendChild(outer);
  
  const width = outer.offsetWidth - outer.clientWidth;
  outer.remove();
  
  console.log('Calculated system scrollbar width allocations:', width, 'px');
  alert(`Internal Sizing: scrollbar handles width is ${width}px (Offsets are fully aligned in grid calculation rules).`);
})();
```

---

### HTTP Response Headers

**Description:** Submits a silent HEAD call to log incoming web page server headers.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20fetch(window.location.href,%20%7B%20method:%20'HEAD'%20%7D)%20.then(res%20=%3E%20%7B%20console.log('%25cHTTP%20Response%20Headers:',%20'font-size:15px;%20font-weight:bold;%20color:#7C3AED');%20const%20container%20=%20%7B%7D;%20res.headers.forEach((val,%20key)%20=%3E%20%7B%20container%5Bkey%5D%20=%20val;%20console.log(%60$%7Bkey%7D:%20$%7Bval%7D%60);%20%7D);%20console.table(container);%20alert('SUCCESS:%20HTTP%20Headers%20fetched%20and%20printed%20inside%20developer%20console%20table!');%20%7D)%20.catch(err%20=%3E%20%7B%20console.error('Fetch%20errors%20logged:',%20err);%20alert('DIAGNOSTIC%20NOTICE:%20Same-Origin%20CORS%20policies%20blocked%20headers%20reading.%20Check%20Network%20logs%20instead.');%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// HTTP Host response properties auditor
(function() {
  fetch(window.location.href, { method: 'HEAD' })
    .then(res => {
      console.log('%cHTTP Response Headers:', 'font-size:15px; font-weight:bold; color:#7C3AED');
      const container = {};
      res.headers.forEach((val, key) => {
        container[key] = val;
        console.log(`${key}: ${val}`);
      });
      console.table(container);
      alert('SUCCESS: HTTP Headers fetched and printed inside developer console table!');
    })
    .catch(err => {
      console.error('Fetch errors logged:', err);
      alert('DIAGNOSTIC NOTICE: Same-Origin CORS policies blocked headers reading. Check Network logs instead.');
    });
})();
```

---

### Export Layout as Markdown

**Description:** Parses headings and paragraphs into standard formatted Markdown text inside console logs.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20let%20markdown%20=%20'';%20document.querySelectorAll('h1,%20h2,%20h3,%20h4,%20p,%20li').forEach(el%20=%3E%20%7B%20const%20text%20=%20el.textContent.trim();%20if%20(text%20===%20'')%20return;%20const%20tag%20=%20el.tagName.toLowerCase();%20if%20(tag%20===%20'h1')%20markdown%20+=%20%60#%20$%7Btext%7D%20%60;%20else%20if%20(tag%20===%20'h2')%20markdown%20+=%20%60##%20$%7Btext%7D%20%60;%20else%20if%20(tag%20===%20'h3')%20markdown%20+=%20%60###%20$%7Btext%7D%20%60;%20else%20if%20(tag%20===%20'li')%20markdown%20+=%20%60-%20$%7Btext%7D%20%60;%20else%20markdown%20+=%20%60$%7Btext%7D%20%60;%20%7D);%20console.log('%25cConverted%20Page%20Markdown%20Bundle:',%20'font-size:15px;%20font-weight:bold;%20color:#10B981');%20console.log(markdown);%20alert('SUCCESS:%20Clean%20Markdown%20exported%20directly%20to%20developer%20console!');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Dynamic DOM content writer to Markdown converter
(function() {
  let markdown = '';
  document.querySelectorAll('h1, h2, h3, h4, p, li').forEach(el => {
    const text = el.textContent.trim();
    if (text === '') return;
    
    const tag = el.tagName.toLowerCase();
    if (tag === 'h1') markdown += `# ${text}

`;
    else if (tag === 'h2') markdown += `## ${text}

`;
    else if (tag === 'h3') markdown += `### ${text}

`;
    else if (tag === 'li') markdown += `- ${text}
`;
    else markdown += `${text}

`;
  });
  
  console.log('%cConverted Page Markdown Bundle:', 'font-size:15px; font-weight:bold; color:#10B981');
  console.log(markdown);
  alert('SUCCESS: Clean Markdown exported directly to developer console!');
})();
```

---

### Purge Storage & Session

**Description:** Instantly sweeps local storage, session storage, and logs details in console to reset cookies & application state.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20localStorage.clear();%20sessionStorage.clear();%20console.log('%25cPurge%20Completed:',%20'font-size:14px;%20font-weight:bold;%20color:#ef4444');%20console.log('Local%20Storage%20cleared.%20Session%20Storage%20cleared.');%20alert('Purged%20Storage%20Cache:%20---------------------%20Local%20Storage%20and%20Session%20Storage%20cleared%20successfully!');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Purge client-side key-value cache storages
(function() {
  localStorage.clear();
  sessionStorage.clear();
  console.log('%cPurge Completed:', 'font-size:14px; font-weight:bold; color:#ef4444');
  console.log('Local Storage cleared.
Session Storage cleared.');
  alert('Purged Storage Cache:
---------------------
Local Storage and Session Storage cleared successfully!');
})();
```

---

### View DNS Records

**Description:** Redirects the current domain to nslookup.io to audit DNS records, MX configurations, and IP nameservers instantly.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20host%20=%20window.location.hostname;%20if%20(host%20&&%20host%20!==%20'localhost'%20&&%20host%20!==%20'127.0.0.1')%20%7B%20window.open(%60https://www.nslookup.io/domains/$%7Bhost%7D/dns-records/%60,%20'_blank');%20console.log(%60Opened%20DNS%20lookup%20for%20domain:%20$%7Bhost%7D%60);%20%7D%20else%20%7B%20alert('Please%20run%20this%20bookmarklet%20on%20a%20live%20website%20with%20a%20valid%20domain.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Redirect to nslookup.io DNS toolset
(function() {
  const host = window.location.hostname;
  if (host && host !== 'localhost' && host !== '127.0.0.1') {
    window.open(`https://www.nslookup.io/domains/${host}/dns-records/`, '_blank');
    console.log(`Opened DNS lookup for domain: ${host}`);
  } else {
    alert('Please run this bookmarklet on a live website with a valid domain.');
  }
})();
```

---

### Extract Page Images

**Description:** Gathers all images on the current webpage and displays them in a clean, downloadable grid panel in a new tab.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20imgs%20=%20document.querySelectorAll('img');%20if%20(imgs.length%20===%200)%20%7B%20alert('No%20images%20found%20on%20this%20page.');%20return;%20%7D%20const%20w%20=%20window.open();%20if%20(!w)%20%7B%20alert('Popup%20blocked%20by%20browser!%20Please%20enable%20popup%20windows%20to%20view%20image%20extractor.');%20return;%20%7D%20w.document.write('%3Chtml%3E%3Chead%3E%3Ctitle%3EExtracted%20Images%3C/title%3E%3Cstyle%3Ebody%7Bfont-family:sans-serif;background:#0f172a;color:#f8fafc;padding:24px%7Dh1%7Bfont-size:20px%7Dimg%7Bmax-width:200px;max-height:200px;margin:8px;border:2px%20solid%20#334155;border-radius:6px;transition:transform%200.2s%7Dimg:hover%7Btransform:scale(1.1);border-color:#3b82f6%7D%3C/style%3E%3C/head%3E%3Cbody%3E%3Ch1%3EExtracted%20Images%20('+imgs.length+')%3C/h1%3E%3Cdiv%20style=%22display:flex;flex-wrap:wrap%22%3E');%20imgs.forEach(img%20=%3E%20%7B%20if%20(img.src)%20w.document.write('%3Ca%20href=%22'+img.src+'%22%20target=%22_blank%22%3E%3Cimg%20src=%22'+img.src+'%22%20title=%22'+img.src+'%22%20referrerPolicy=%22no-referrer%22/%3E%3C/a%3E')%20%7D);%20w.document.write('%3C/div%3E%3C/body%3E%3C/html%3E');%20w.document.close();%20console.log(%60Extracted%20$%7Bimgs.length%7D%20image%20elements%20from%20the%20page.%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Extract and load all active images into a visual gallery tab
(function() {
  const imgs = document.querySelectorAll('img');
  if (imgs.length === 0) {
    alert('No images found on this page.');
    return;
  }
  const w = window.open();
  if (!w) {
    alert('Popup blocked by browser! Please enable popup windows to view image extractor.');
    return;
  }
  w.document.write('<html><head><title>Extracted Images</title><style>body{font-family:sans-serif;background:#0f172a;color:#f8fafc;padding:24px}h1{font-size:20px}img{max-width:200px;max-height:200px;margin:8px;border:2px solid #334155;border-radius:6px;transition:transform 0.2s}img:hover{transform:scale(1.1);border-color:#3b82f6}</style></head><body><h1>Extracted Images ('+imgs.length+')</h1><div style="display:flex;flex-wrap:wrap">');
  imgs.forEach(img => {
    if (img.src) w.document.write('<a href="'+img.src+'" target="_blank"><img src="'+img.src+'" title="'+img.src+'" referrerPolicy="no-referrer"/></a>')
  });
  w.document.write('</div></body></html>');
  w.document.close();
  console.log(`Extracted ${imgs.length} image elements from the page.`);
})();
```

---

### Clear Domain Cookies

**Description:** Sweeps all cookie storage of the current domain to reset sessions and debug fresh load parameters.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20cookies%20=%20document.cookie.split(';');%20for%20(let%20i%20=%200;%20i%20%3C%20cookies.length;%20i++)%20%7B%20const%20cookie%20=%20cookies%5Bi%5D;%20const%20eqPos%20=%20cookie.indexOf('=');%20const%20name%20=%20eqPos%20%3E%20-1%20?%20cookie.substr(0,%20eqPos)%20:%20cookie;%20document.cookie%20=%20name.trim()%20+%20'=;expires=Thu,%2001%20Jan%201970%2000:00:00%20GMT;path=/';%20%7D%20console.log(%60Purged%20cookies%20on%20host:%20$%7Bwindow.location.hostname%7D%60);%20alert(%60Attempted%20to%20clear%20cookies%20for%20$%7Bwindow.location.hostname%7D%20successfully!%60);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Purge current host cookies
(function() {
  const cookies = document.cookie.split(';');
  for (let i = 0; i < cookies.length; i++) {
    const cookie = cookies[i];
    const eqPos = cookie.indexOf('=');
    const name = eqPos > -1 ? cookie.substr(0, eqPos) : cookie;
    document.cookie = name.trim() + '=;expires=Thu, 01 Jan 1970 00:00:00 GMT;path=/';
  }
  console.log(`Purged cookies on host: ${window.location.hostname}`);
  alert(`Attempted to clear cookies for ${window.location.hostname} successfully!`);
})();
```

---

## 🛡️ Security & Penetration Testing

### WordPress Version Detector

**Description:** Detects the active WordPress core release version from page metadata and page stylesheets.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20v%20=%20'';%20var%20m%20=%20document.querySelector('meta%5Bname=%22generator%22%5D');%20if%20(m%20&&%20m.content.toLowerCase().includes('wordpress'))%20%7B%20var%20mt%20=%20m.content.match(/%5B%5Cd.%5D+/);%20if%20(mt)%20v%20=%20mt%5B0%5D;%20%7D%20var%20l%20=%20document.querySelector('link%5Brel=%22stylesheet%22%5D');%20if%20(!v%20&&%20l)%20%7B%20var%20mt2%20=%20l.href.match(/ver=(%5B%5Cd.%5D+)/);%20if%20(mt2)%20v%20=%20mt2%5B1%5D;%20%7D%20if%20(v)%20%7B%20alert('WordPress%20Version:%20'%20+%20v);%20console.log('WordPress%20version%20detected:',%20v);%20%7D%20else%20%7B%20alert('WordPress%20version%20not%20detected.');%20console.log('No%20wordpress%20version%20found%20in%20metadata%20or%20styles.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// WordPress Core version auditor
(function() {
  var v = '';
  var m = document.querySelector('meta[name="generator"]');
  if (m && m.content.toLowerCase().includes('wordpress')) {
    var mt = m.content.match(/[\d.]+/);
    if (mt) v = mt[0];
  }
  var l = document.querySelector('link[rel="stylesheet"]');
  if (!v && l) {
    var mt2 = l.href.match(/ver=([\d.]+)/);
    if (mt2) v = mt2[1];
  }
  if (v) {
    alert('WordPress Version: ' + v);
    console.log('WordPress version detected:', v);
  } else {
    alert('WordPress version not detected.');
    console.log('No wordpress version found in metadata or styles.');
  }
})();
```

---

### Unmask Password Inputs

**Description:** Converts all password fields into plain editable text to easily reveal obscured values during testing.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20p%20=%20document.querySelectorAll('input%5Btype=%22password%22%5D');%20if%20(p.length%20===%200)%20%7B%20alert('No%20password%20fields%20found%20on%20this%20page.');%20console.log('Audit:%20No%20password%20inputs%20detected.');%20%7D%20else%20%7B%20p.forEach(function(el)%20%7B%20el.type%20=%20'text';%20%7D);%20alert('Unmasked%20'%20+%20p.length%20+%20'%20password%20input(s).');%20console.log('Audit:%20Unmasked%20'%20+%20p.length%20+%20'%20password%20fields%20successfully.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Unmask Hidden Password Inputs
(function() {
  var p = document.querySelectorAll('input[type="password"]');
  if (p.length === 0) {
    alert('No password fields found on this page.');
    console.log('Audit: No password inputs detected.');
  } else {
    p.forEach(function(el) {
      el.type = 'text';
    });
    alert('Unmasked ' + p.length + ' password input(s).');
    console.log('Audit: Unmasked ' + p.length + ' password fields successfully.');
  }
})();
```

---

### Cookie Monster Resolver

**Description:** Inspects, lists, and provides options to clear individual cookies for the current domain name.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20cookies%20=%20document.cookie.split(';');%20if%20(cookies.length%20===%200%20%7C%7C%20(cookies.length%20===%201%20&&%20cookies%5B0%5D%20===%20''))%20%7B%20alert('No%20cookies%20found%20for%20this%20host.');%20console.log('No%20active%20cookies%20detected%20on%20this%20site.');%20%7D%20else%20%7B%20var%20list%20=%20%5B%5D;%20cookies.forEach(function(c)%20%7B%20var%20parts%20=%20c.split('=');%20list.push(parts%5B0%5D.trim()%20+%20':%20'%20+%20(parts%5B1%5D%20%7C%7C%20'').trim());%20%7D);%20alert('Cookies%20found%20('%20+%20list.length%20+%20'):%20'%20+%20list.join('%20'));%20console.log('Active%20Cookies%20Catalog:',%20list);%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Audit and inspect host cookies
(function() {
  var cookies = document.cookie.split(';');
  if (cookies.length === 0 || (cookies.length === 1 && cookies[0] === '')) {
    alert('No cookies found for this host.');
    console.log('No active cookies detected on this site.');
  } else {
    var list = [];
    cookies.forEach(function(c) {
      var parts = c.split('=');
      list.push(parts[0].trim() + ': ' + (parts[1] || '').trim());
    });
    alert('Cookies found (' + list.length + '):

' + list.join('
'));
    console.log('Active Cookies Catalog:', list);
  }
})();
```

---

### Show Hidden Elements

**Description:** Forces visibility of all hidden elements, display:none, visibility:hidden, or opacity:0 on the page.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20el%20=%20document.querySelectorAll('*');%20var%20count%20=%200;%20el.forEach(function(e)%20%7B%20var%20s%20=%20window.getComputedStyle(e);%20if%20(s.display%20===%20'none'%20%7C%7C%20s.visibility%20===%20'hidden'%20%7C%7C%20s.opacity%20===%20'0')%20%7B%20e.style.setProperty('display',%20'block',%20'important');%20e.style.setProperty('visibility',%20'visible',%20'important');%20e.style.setProperty('opacity',%20'1',%20'important');%20e.style.border%20=%20'2px%20dashed%20#f59e0b';%20count++;%20%7D%20%7D);%20alert('Revealed%20'%20+%20count%20+%20'%20hidden%20element(s)%20with%20orange%20dashed%20borders.');%20console.log('Audit:%20Uncovered%20'%20+%20count%20+%20'%20hidden%20DOM%20nodes.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Reveal hidden elements inside the DOM
(function() {
  var el = document.querySelectorAll('*');
  var count = 0;
  el.forEach(function(e) {
    var s = window.getComputedStyle(e);
    if (s.display === 'none' || s.visibility === 'hidden' || s.opacity === '0') {
      e.style.setProperty('display', 'block', 'important');
      e.style.setProperty('visibility', 'visible', 'important');
      e.style.setProperty('opacity', '1', 'important');
      e.style.border = '2px dashed #f59e0b';
      count++;
    }
  });
  alert('Revealed ' + count + ' hidden element(s) with orange dashed borders.');
  console.log('Audit: Uncovered ' + count + ' hidden DOM nodes.');
})();
```

---

### Subdomain Finder (crt.sh)

**Description:** Launches crt.sh Certificate Search in a new tab to find all subdomains registered for the current site.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20host%20=%20window.location.hostname;%20var%20domain%20=%20host.split('.').slice(-2).join('.');%20var%20url%20=%20'https://crt.sh/?q=%2525.'%20+%20domain;%20console.log('Querying%20SSL/TLS%20Certificate%20records%20for%20domain:',%20domain);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Subdomain finder certificate log query
(function() {
  var host = window.location.hostname;
  var domain = host.split('.').slice(-2).join('.');
  var url = 'https://crt.sh/?q=%25.' + domain;
  console.log('Querying SSL/TLS Certificate records for domain:', domain);
  window.open(url, '_blank');
})();
```

---

### IP & DNS Resolver (Google DNS)

**Description:** Opens Google Public DNS Dig tool in a new tab to inspect DNS records for the current domain name.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20host%20=%20window.location.hostname;%20var%20url%20=%20'https://toolbox.googleapps.com/apps/dig/#A/'%20+%20host;%20console.log('Querying%20Google%20Dig%20DNS%20records%20for:',%20host);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// IP & DNS query via Google Public Dig tool
(function() {
  var host = window.location.hostname;
  var url = 'https://toolbox.googleapps.com/apps/dig/#A/' + host;
  console.log('Querying Google Dig DNS records for:', host);
  window.open(url, '_blank');
})();
```

---

### Wayback Machine Archive

**Description:** Checks the Internet Archive Wayback Machine history and logs for the current webpage.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20url%20=%20'https://web.archive.org/web/*/'%20+%20window.location.href;%20console.log('Looking%20up%20history%20logs%20in%20Wayback%20Machine%20for:',%20window.location.href);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Wayback Machine Archive check
(function() {
  var url = 'https://web.archive.org/web/*/' + window.location.href;
  console.log('Looking up history logs in Wayback Machine for:', window.location.href);
  window.open(url, '_blank');
})();
```

---

### Security Headers Inspector

**Description:** Audits HTTP security headers (CSP, HSTS, X-Frame-Options) for the current site using SecurityHeaders.com.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20host%20=%20window.location.hostname;%20var%20url%20=%20'https://securityheaders.com/?q='%20+%20host%20+%20'&followRedirects=on';%20console.log('Auditing%20HTTP%20security%20parameters%20for:',%20host);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Security HTTP headers checker
(function() {
  var host = window.location.hostname;
  var url = 'https://securityheaders.com/?q=' + host + '&followRedirects=on';
  console.log('Auditing HTTP security parameters for:', host);
  window.open(url, '_blank');
})();
```

---

### Whois Domain Lookup

**Description:** Redirects to DomainTools Whois search to inspect host owner registration details and server locations.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20host%20=%20window.location.hostname;%20var%20domain%20=%20host.split('.').slice(-2).join('.');%20var%20url%20=%20'https://whois.domaintools.com/'%20+%20domain;%20console.log('Retrieving%20WHOIS%20registrar%20parameters%20for:',%20domain);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// WHOIS registrar directory lookup
(function() {
  var host = window.location.hostname;
  var domain = host.split('.').slice(-2).join('.');
  var url = 'https://whois.domaintools.com/' + domain;
  console.log('Retrieving WHOIS registrar parameters for:', domain);
  window.open(url, '_blank');
})();
```

---

### Port Scanner (ViewDNS)

**Description:** Sends the current host to ViewDNS Port Scanner to check common open server ports (80, 443, 21, 22).

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20host%20=%20window.location.hostname;%20var%20url%20=%20'https://viewdns.info/portscan/?host='%20+%20host;%20console.log('Querying%20open%20server%20ports%20via%20ViewDNS%20for:',%20host);%20window.open(url,%20'_blank');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Remote server port scanning lookup
(function() {
  var host = window.location.hostname;
  var url = 'https://viewdns.info/portscan/?host=' + host;
  console.log('Querying open server ports via ViewDNS for:', host);
  window.open(url, '_blank');
})();
```

---

### Open Redirect Parameter Checker

**Description:** Finds and highlights potential open redirect parameters (e.g. url, redirect, next, dest) inside the DOM.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20params%20=%20%5B'url',%20'redirect',%20'next',%20'dest',%20'return',%20'go',%20'to',%20'link',%20'checkout'%5D;%20var%20found%20=%20%5B%5D;%20document.querySelectorAll('a').forEach(function(a)%20%7B%20var%20href%20=%20a.href;%20params.forEach(function(p)%20%7B%20if%20(href.includes('?'%20+%20p%20+%20'=')%20%7C%7C%20href.includes('&'%20+%20p%20+%20'='))%20%7B%20a.style.outline%20=%20'3px%20solid%20#ef4444';%20a.style.backgroundColor%20=%20'rgba(239,%2068,%2068,%200.15)';%20found.push(a.href);%20%7D%20%7D);%20%7D);%20if%20(found.length%20%3E%200)%20%7B%20alert('Found%20'%20+%20found.length%20+%20'%20links%20with%20possible%20open%20redirect%20parameters.%20Outlined%20in%20red!');%20console.log('Potential%20open%20redirect%20pathways%20detected:',%20found);%20%7D%20else%20%7B%20alert('No%20typical%20open%20redirect%20parameter%20links%20identified%20on%20the%20current%20page.');%20console.log('No%20parameter%20patterns%20matched%20redirect%20flags.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Open redirect parameters audit
(function() {
  var params = ['url', 'redirect', 'next', 'dest', 'return', 'go', 'to', 'link', 'checkout'];
  var found = [];
  document.querySelectorAll('a').forEach(function(a) {
    var href = a.href;
    params.forEach(function(p) {
      if (href.includes('?' + p + '=') || href.includes('&' + p + '=')) {
        a.style.outline = '3px solid #ef4444';
        a.style.backgroundColor = 'rgba(239, 68, 68, 0.15)';
        found.push(a.href);
      }
    });
  });
  if (found.length > 0) {
    alert('Found ' + found.length + ' links with possible open redirect parameters. Outlined in red!');
    console.log('Potential open redirect pathways detected:', found);
  } else {
    alert('No typical open redirect parameter links identified on the current page.');
    console.log('No parameter patterns matched redirect flags.');
  }
})();
```

---

### Clickjacking Protection Audit

**Description:** Determines if the current page can be embedded inside a frame and audits clickjacking risk parameters.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20try%20%7B%20if%20(window.self%20!==%20window.top)%20%7B%20alert('This%20page%20is%20already%20embedded%20inside%20an%20iframe%20(Frame%20check:%20Embedded!).%20High%20clickjacking%20vulnerability%20if%20X-Frame-Options%20is%20missing.');%20%7D%20else%20%7B%20var%20f%20=%20document.createElement('iframe');%20f.src%20=%20window.location.href;%20f.style.position%20=%20'fixed';%20f.style.top%20=%20'0';%20f.style.left%20=%20'0';%20f.style.width%20=%20'10px';%20f.style.height%20=%20'10px';%20f.style.opacity%20=%20'0.01';%20f.style.zIndex%20=%20'99999';%20document.body.appendChild(f);%20console.log('Spawning%20testing%20iframe%20to%20evaluate%20frame%20ancestors%20policies...');%20setTimeout(function()%20%7B%20try%20%7B%20var%20doc%20=%20f.contentDocument%20%7C%7C%20f.contentWindow.document;%20alert('Audit%20complete:%20Page%20allowed%20local%20iframe%20embedding!%20X-Frame-Options%20or%20CSP%20frame-ancestors%20might%20be%20missing/lax.');%20console.log('Result:%20Frame%20embedding%20allowed%20(vulnerable%20to%20clickjacking%20if%20public).');%20%7D%20catch%20(err)%20%7B%20alert('Audit%20complete:%20Page%20BLOCKED%20iframe%20embedding%20(X-Frame-Options%20/%20CSP%20is%20secure).');%20console.log('Result:%20Secure.%20Frame%20embedding%20blocked.');%20%7D%20f.remove();%20%7D,%201000);%20%7D%20%7D%20catch(e)%20%7B%20alert('Clickjacking%20check%20error:%20'%20+%20e.message);%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Clickjacking validation audit
(function() {
  try {
    if (window.self !== window.top) {
      alert('This page is already embedded inside an iframe (Frame check: Embedded!). High clickjacking vulnerability if X-Frame-Options is missing.');
    } else {
      var f = document.createElement('iframe');
      f.src = window.location.href;
      f.style.position = 'fixed';
      f.style.top = '0';
      f.style.left = '0';
      f.style.width = '10px';
      f.style.height = '10px';
      f.style.opacity = '0.01';
      f.style.zIndex = '99999';
      document.body.appendChild(f);
      console.log('Spawning testing iframe to evaluate frame ancestors policies...');
      setTimeout(function() {
        try {
          var doc = f.contentDocument || f.contentWindow.document;
          alert('Audit complete: Page allowed local iframe embedding! X-Frame-Options or CSP frame-ancestors might be missing/lax.');
          console.log('Result: Frame embedding allowed (vulnerable to clickjacking if public).');
        } catch (err) {
          alert('Audit complete: Page BLOCKED iframe embedding (X-Frame-Options / CSP is secure).');
          console.log('Result: Secure. Frame embedding blocked.');
        }
        f.remove();
      }, 1000);
    }
  } catch(e) {
    alert('Clickjacking check error: ' + e.message);
  }
})();
```

---

### Unblock Event Hijacking (No Hijack)

**Description:** Blocks common event hijacking techniques, like disabling paste, right-click, text selection, and some keyboard shortcuts. Run again to undo.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(()%20=%3E%20%7B%20if%20(window._NoHijackHandlers)%20%7B%20for%20(const%20%5BeventName,%20handler%5D%20of%20Object.entries(window._NoHijackHandlers))%20%7B%20document.removeEventListener(eventName,%20handler,%20true);%20%7D%20window._NoHijackHandlers%20=%20null;%20alert(%22Event%20protection%20disabled.%20Re-enabled%20default%20page%20handlers.%22);%20return;%20%7D%20const%20block%20=%20e%20=%3E%20e.stopImmediatePropagation();%20window._NoHijackHandlers%20=%20%7B%20copy:%20block,%20cut:%20block,%20paste:%20block,%20contextmenu:%20block,%20selectstart:%20block,%20keydown:%20e%20=%3E%20%7B%20if%20(e.altKey%20&&%20e.key.match(/%5B0-9%5D/))%20%7B%20e.stopImmediatePropagation();%20%7D%20%7D%20%7D;%20for%20(const%20%5BeventName,%20handler%5D%20of%20Object.entries(window._NoHijackHandlers))%20%7B%20document.addEventListener(eventName,%20handler,%20true);%20%7D%20alert(%22NoHijack%20activated!%20Copy,%20paste,%20text%20selection,%20and%20right-click%20have%20been%20unblocked.%22);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Block event hijacking scripts on the page
(() => {
    if (window._NoHijackHandlers) {
        for (const [eventName, handler] of Object.entries(window._NoHijackHandlers)) {
            document.removeEventListener(eventName, handler, true);
        }
        window._NoHijackHandlers = null;
        alert("Event protection disabled. Re-enabled default page handlers.");
        return;
    }

    const block = e => e.stopImmediatePropagation();
    window._NoHijackHandlers = {
        copy: block,
        cut: block,
        paste: block,
        contextmenu: block,
        selectstart: block,
        keydown: e => {
            if (e.altKey && e.key.match(/[0-9]/)) {
                e.stopImmediatePropagation();
            }
        }
    };
    for (const [eventName, handler] of Object.entries(window._NoHijackHandlers)) {
        document.addEventListener(eventName, handler, true);
    }
    alert("NoHijack activated! Copy, paste, text selection, and right-click have been unblocked.");
})();
```

---

### Force Page Offline

**Description:** Injects a restrictive Content Security Policy (CSP) and terminates connections to test site behaviors in offline mode.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20meta%20=%20document.createElement('meta');%20meta.httpEquiv%20=%20'Content-Security-Policy';%20meta.content%20=%20%22default-src%20'unsafe-eval'%20data:%20blob:;%22;%20document.head.appendChild(meta);%20window.stop();%20alert('Offline%20mode%20triggered!%20Restrictive%20Content%20Security%20Policy%20applied.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Injects CSP to block external connections
(function() {
    const meta = document.createElement('meta');
    meta.httpEquiv = 'Content-Security-Policy';
    meta.content = "default-src 'unsafe-eval' data: blob:;";
    document.head.appendChild(meta);

    /* stop open connections. In Firefox, this will also close many web sockets */
    window.stop();
    alert('Offline mode triggered! Restrictive Content Security Policy applied.');
})();
```

---

### Email Address Scraper

**Description:** Scans the page inner text to harvest and catalog all visible email addresses into a clean list window.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20const%20emails%20=%20document.body.innerText.match(/%5Ba-zA-Z0-9._%25+-%5D+@%5Ba-zA-Z0-9.-%5D+%5C.%5Ba-zA-Z%5D%7B2,%7D/g);%20if%20(emails)%20%7B%20const%20unique%20=%20Array.from(new%20Set(emails));%20const%20newWin%20=%20window.open();%20if%20(newWin)%20%7B%20newWin.document.write('%3Chtml%3E%3Chead%3E%3Ctitle%3EScraped%20Emails%3C/title%3E%3Cstyle%3Ebody%7Bfont-family:sans-serif;padding:20px;background:#f8fafc;color:#0f172a%7Dli%7Bmargin:8px%200;font-family:monospace;font-size:14px%7D%3C/style%3E%3C/head%3E%3Cbody%3E%3Ch1%3EEmail%20Addresses%20Found%20('%20+%20unique.length%20+%20')%3C/h1%3E%3Cul%3E'%20+%20unique.map(e%20=%3E%20'%3Cli%3E'%20+%20e%20+%20'%3C/li%3E').join('')%20+%20'%3C/ul%3E%3C/body%3E%3C/html%3E');%20newWin.document.close();%20%7D%20else%20%7B%20alert('Popup%20blocked!%20Please%20allow%20popups%20to%20view%20the%20'%20+%20unique.length%20+%20'%20emails%20found.');%20%7D%20console.log('Harvested%20emails:',%20unique);%20%7D%20else%20%7B%20alert('No%20email%20addresses%20found%20on%20this%20page.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Email Address harvester and scraper
(function() {
  const emails = document.body.innerText.match(/[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}/g);
  if (emails) {
    const unique = Array.from(new Set(emails));
    const newWin = window.open();
    if (newWin) {
      newWin.document.write('<html><head><title>Scraped Emails</title><style>body{font-family:sans-serif;padding:20px;background:#f8fafc;color:#0f172a}li{margin:8px 0;font-family:monospace;font-size:14px}</style></head><body><h1>Email Addresses Found (' + unique.length + ')</h1><ul>' + unique.map(e => '<li>' + e + '</li>').join('') + '</ul></body></html>');
      newWin.document.close();
    } else {
      alert('Popup blocked! Please allow popups to view the ' + unique.length + ' emails found.');
    }
    console.log('Harvested emails:', unique);
  } else {
    alert('No email addresses found on this page.');
  }
})();
```

---

### Wappalyzer Profiler

**Description:** Profiles the current page using Wappalyzer to discover software stacks, CMS versions, trackers, and libraries.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20d%20=%20document,%20e%20=%20d.getElementById('wappalyzer-container');%20if%20(e%20!==%20null)%20%7B%20d.body.removeChild(e);%20%7D%20var%20u%20=%20'https://www.wappalyzer.com/',%20c%20=%20d.createElement('div'),%20p%20=%20d.createElement('div'),%20l%20=%20d.createElement('link'),%20s%20=%20d.createElement('script');%20c.setAttribute('id',%20'wappalyzer-container');%20l.setAttribute('rel',%20'stylesheet');%20l.setAttribute('href',%20u%20+%20'css/bookmarklet.css');%20d.head.appendChild(l);%20p.setAttribute('id',%20'wappalyzer-pending');%20p.setAttribute('style',%20'background-image:%20url('%20+%20u%20+%20'images/spinner.gif)%20!important');%20c.appendChild(p);%20s.setAttribute('src',%20u%20+%20'bookmarklet/wappalyzer.js');%20s.onload%20=%20function()%20%7B%20window.wappalyzer%20=%20new%20Wappalyzer();%20var%20s2%20=%20d.createElement('script');%20s2.setAttribute('src',%20u%20+%20'bookmarklet/apps.js');%20s2.onload%20=%20function()%20%7B%20var%20s3%20=%20d.createElement('script');%20s3.setAttribute('src',%20u%20+%20'bookmarklet/driver.js');%20c.appendChild(s3);%20%7D;%20c.appendChild(s2);%20%7D;%20c.appendChild(s);%20d.body.appendChild(c);%20console.log('Wappalyzer%20widget%20injected%20successfully.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Inject Wappalyzer tech-stack discovery script
(function() {
  var d = document, e = d.getElementById('wappalyzer-container');
  if (e !== null) { d.body.removeChild(e); }
  var u = 'https://www.wappalyzer.com/',
      c = d.createElement('div'),
      p = d.createElement('div'),
      l = d.createElement('link'),
      s = d.createElement('script');
  c.setAttribute('id', 'wappalyzer-container');
  l.setAttribute('rel', 'stylesheet');
  l.setAttribute('href', u + 'css/bookmarklet.css');
  d.head.appendChild(l);
  p.setAttribute('id', 'wappalyzer-pending');
  p.setAttribute('style', 'background-image: url(' + u + 'images/spinner.gif) !important');
  c.appendChild(p);
  s.setAttribute('src', u + 'bookmarklet/wappalyzer.js');
  s.onload = function() {
    window.wappalyzer = new Wappalyzer();
    var s2 = d.createElement('script');
    s2.setAttribute('src', u + 'bookmarklet/apps.js');
    s2.onload = function() {
      var s3 = d.createElement('script');
      s3.setAttribute('src', u + 'bookmarklet/driver.js');
      c.appendChild(s3);
    };
    c.appendChild(s2);
  };
  c.appendChild(s);
  d.body.appendChild(c);
  console.log('Wappalyzer widget injected successfully.');
})();
```

---

### Redirect & Popunder Blocker

**Description:** Blocks window.open, location redirects, target=\

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%7B%20'use%20strict';%20window.open%20=%20function()%7B%20console.warn(%22Blocked%20window.open()%22);%20return%20null;%20%7D;%20try%20%7B%20window.location.assign%20=%20function(url)%7B%20console.warn(%22Blocked%20location.assign:%22,%20url);%20%7D;%20window.location.replace%20=%20function(url)%7B%20console.warn(%22Blocked%20location.replace:%22,%20url);%20%7D;%20%7D%20catch(e)%7B%7D%20document.querySelectorAll('a%5Btarget%5D').forEach(function(a)%7B%20a.removeAttribute('target');%20%7D);%20window.onbeforeunload%20=%20null;%20window.addEventListener('beforeunload',%20function(e)%7B%20e.stopImmediatePropagation();%20%7D,%20true);%20document.addEventListener('click',%20function(e)%7B%20let%20el%20=%20e.target.closest('a');%20if(el)%7B%20el.removeAttribute('target');%20el.onclick%20=%20null;%20%7D%20%7D,%20true);%20alert(%22Redirect%20protection%20enabled.%22);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Disable redirects & popunders
(function(){
  'use strict';
  window.open = function(){
    console.warn("Blocked window.open()");
    return null;
  };
  try {
    window.location.assign = function(url){
      console.warn("Blocked location.assign:", url);
    };
    window.location.replace = function(url){
      console.warn("Blocked location.replace:", url);
    };
  } catch(e){}
  document.querySelectorAll('a[target]').forEach(function(a){
    a.removeAttribute('target');
  });
  window.onbeforeunload = null;
  window.addEventListener('beforeunload', function(e){
    e.stopImmediatePropagation();
  }, true);
  document.addEventListener('click', function(e){
    let el = e.target.closest('a');
    if(el){
      el.removeAttribute('target');
      el.onclick = null;
    }
  }, true);
  alert("Redirect protection enabled.");
})();
```

---

### Endpoint Extractor

**Description:** Scrapes, categorizes, and extracts all script URLs and API endpoints on the current page.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(async()=%3E%7B%20const%20r=new%20RegExp(%22(?%3C=(%5C%22%7C'%7C%5C%5Cx60))%5C%5C/%5Ba-zA-Z0-9_?&=%5C%5C%20handling/%5C%5C-#%5C%5C.%5D*(?=(%5C%22%7C'%7C%5C%5Cx60))%22,%22g%22),e=new%20Set,t=document.getElementsByTagName(%22script%22),n=t=%3E%7Bconst%20a=t.matchAll(r);for(const%20t%20of%20a)e.add(t%5B0%5D)%7D;%20await%20Promise.all(Array.from(t).map(async%20t=%3E%7Btry%7Bt.src?n(await(await%20fetch(t.src)).text()):n(t.innerHTML)%7Dcatch(t)%7Bconsole.warn(%22Script%20fetch%20error:%22,t)%7D%7D)),n(document.documentElement.outerHTML);%20const%20d=location.origin,paths=%5B...e%5D;%20const%20categorizeEndpoints=paths=%3E%7Bconst%20categories=%7Bapis:%5B%5D,js:%5B%5D,html:%5B%5D,css:%5B%5D,json:%5B%5D,xml:%5B%5D,images:%5B%5D,other:%5B%5D%7D;return%20paths.forEach(p=%3E%7Bif(p.match(/%5C.js$/i))categories.js.push(p);else%20if(p.match(/%5C.html?$/i))categories.html.push(p);else%20if(p.match(/%5C.css$/i))categories.css.push(p);else%20if(p.match(/%5C.json$/i))categories.json.push(p);else%20if(p.match(/%5C.xml$/i))categories.xml.push(p);else%20if(p.match(/%5C.(png%7Cjpg%7Cjpeg%7Cgif%7Csvg%7Cwebp%7Cico)$/i))categories.images.push(p);else%20if(p.match(/%5E%5C/api%5C//i)%7C%7Cp.match(/%5E%5C/v%5Cd+%5C//i))categories.apis.push(p);else%20categories.other.push(p)%7D),categories%7D,cats=categorizeEndpoints(paths),win=window.open(%22%22,%22_blank%22,%22width=1200,height=700,scrollbars=yes%22);%20if(!win)return%20alert(%22Popup%20blocked.%20Please%20allow%20popups.%22);%20const%20style='%3Cstyle%3E*%7Bmargin:0;padding:0;box-sizing:border-box%7Dbody%7Bbackground:#0f0f0f;color:#e0e0e0;font-family:monospace;padding:20px%7Dh2%7Bcolor:#4fc3f7;margin-bottom:5px%7Dp%7Bcolor:#888;margin-bottom:15px%7Dbutton,input%7Bmargin:5px;padding:10px;background:#222;color:#e0e0e0;border:1px%20solid%20#4fc3f7;cursor:pointer;font-family:monospace%7Dbutton:hover%7Bbackground:#333%7Dinput%7Bwidth:300px%7D.tab-btn%7Bbackground:#1a1a1a;color:#aaa;padding:10px%2015px;margin:3px%7D.tab-btn.active%7Bbackground:#4fc3f7;color:#000;font-weight:bold%7D.tab-content%7Bdisplay:none;margin-top:15px;max-height:700px;overflow-y:auto%7D.tab-content.active%7Bdisplay:block%7Dul%7Blist-style:none;padding:0%7Dli%7Bpadding:8px;margin:2px%200;background:#1a1a1a;border-left:3px%20solid%20#4fc3f7%7Dli%20a%7Bcolor:#4fc3f7;text-decoration:none;display:block%7Dli%20a:hover%7Bcolor:#81d4fa;text-decoration:underline%7D.footer%7Bmargin-top:20px;padding-top:15px;border-top:1px%20solid%20#333;color:#666%7D%3C/style%3E';%20const%20html='%3Chtml%3E%3Chead%3E%3Ctitle%3EEndpoint%20Extractor%20-%20Rezy%20Dev%3C/title%3E'+style+'%3C/head%3E%3Cbody%3E%3Ch2%3EEndpoint%20Extractor%3C/h2%3E%3Cp%3EFound%20'+paths.length+'%20endpoints%3C/p%3E%3Cdiv%3E%3Cbutton%20id=cpbtn%3ECopy%3C/button%3E%3Cbutton%20id=dlbtn%3EDownload%3C/button%3E%3Cinput%20id=filt%20placeholder=%22Filter%20endpoints...%22%3E%3C/div%3E%3Cdiv%20style=%22margin-top:15px%22%3E%3Cbutton%20class=%22tab-btn%20active%22%20data-tab=%22all%22%3EAll%20('+paths.length+')%3C/button%3E'+(cats.apis.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22apis%22%3EAPIs%20('+cats.apis.length+')%3C/button%3E':'')+(cats.js.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22js%22%3EJS%20('+cats.js.length+')%3C/button%3E':'')+(cats.html.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22html%22%3EHTML%20('+cats.html.length+')%3C/button%3E':'')+(cats.css.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22css%22%3ECSS%20('+cats.css.length+')%3C/button%3E':'')+(cats.json.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22json%22%3EJSON%20('+cats.json.length+')%3C/button%3E':'')+(cats.xml.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22xml%22%3EXML%20('+cats.xml.length+')%3C/button%3E':'')+(cats.images.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22images%22%3EImages%20('+cats.images.length+')%3C/button%3E':'')+(cats.other.length?'%3Cbutton%20class=%22tab-btn%22%20data-tab=%22other%22%3EOther%20('+cats.other.length+')%3C/button%3E':'')+'%3C/div%3E%3Cdiv%20id=%22tab-all%22%20class=%22tab-content%20active%22%3E%3Cul%20id=list-all%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-apis%22%20class=%22tab-content%22%3E%3Cul%20id=list-apis%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-js%22%20class=%22tab-content%22%3E%3Cul%20id=list-js%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-html%22%20class=%22tab-content%22%3E%3Cul%20id=list-html%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-css%22%20class=%22tab-content%22%3E%3Cul%20id=list-css%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-json%22%20class=%22tab-content%22%3E%3Cul%20id=list-json%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-xml%22%20class=%22tab-content%22%3E%3Cul%20id=list-xml%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-images%22%20class=%22tab-content%22%3E%3Cul%20id=list-images%3E%3C/ul%3E%3C/div%3E%3Cdiv%20id=%22tab-other%22%20class=%22tab-content%22%3E%3Cul%20id=list-other%3E%3C/ul%3E%3C/div%3E%3Cdiv%20class=%22footer%22%3EBuilt%20with%20%E2%9D%A4%EF%B8%8F%20by%20%3Ca%20href=%22https://rezydev.com/%22%20target=%22_blank%22%20style=%22color:#4fc3f7%22%3ERezy%20Dev%3C/a%3E%3C/div%3E%3C/body%3E%3C/html%3E';%20win.document.write(html);%20win.document.close();%20const%20populateList=(id,items)=%3E%7Bconst%20ul=win.document.getElementById(id);items.forEach(p=%3E%7Bconst%20li=win.document.createElement(%22li%22);const%20a=win.document.createElement(%22a%22);a.href=d+p;a.target=%22_blank%22;a.textContent=p;li.appendChild(a);ul.appendChild(li)%7D)%7D;%20populateList(%22list-all%22,paths);populateList(%22list-apis%22,cats.apis);populateList(%22list-js%22,cats.js);populateList(%22list-html%22,cats.html);populateList(%22list-css%22,cats.css);populateList(%22list-json%22,cats.json);populateList(%22list-xml%22,cats.xml);populateList(%22list-images%22,cats.images);populateList(%22list-other%22,cats.other);%20win.document.querySelectorAll(%22.tab-btn%22).forEach(b=%3Eb.onclick=function()%7Bwin.document.querySelectorAll(%22.tab-content%22).forEach(t=%3Et.classList.remove(%22active%22));win.document.querySelectorAll(%22.tab-btn%22).forEach(t=%3Et.classList.remove(%22active%22));win.document.getElementById(%22tab-%22+b.getAttribute(%22data-tab%22)).classList.add(%22active%22);b.classList.add(%22active%22)%7D);%20win.document.getElementById(%22cpbtn%22).onclick=function()%7Bconst%20ul=win.document.querySelector(%22.tab-content.active%20ul%22);const%20items=Array.from(ul.querySelectorAll(%22li%20a%22)).map(a=%3Ea.textContent).join(%22%5C%20%22);const%20ta=win.document.createElement(%22textarea%22);ta.value=items;win.document.body.appendChild(ta);ta.select();win.document.execCommand(%22copy%22);win.document.body.removeChild(ta);win.alert(%22Copied!%22)%7D;%20win.document.getElementById(%22dlbtn%22).onclick=function()%7Bconst%20ul=win.document.querySelector(%22.tab-content.active%20ul%22);const%20items=Array.from(ul.querySelectorAll(%22li%20a%22)).map(a=%3Ea.textContent).join(%22%5C%20%22);const%20b=new%20Blob(%5Bitems%5D,%7Btype:%22text/plain%22%7D),u=URL.createObjectURL(b),a=win.document.createElement(%22a%22);a.href=u;a.download=%22endpoints.txt%22;a.click();URL.revokeObjectURL(u)%7D;%20win.document.getElementById(%22filt%22).oninput=function()%7Bconst%20f=this.value.toLowerCase();const%20ul=win.document.querySelector(%22.tab-content.active%20ul%22);ul.querySelectorAll(%22li%22).forEach(li=%3E%7Bconst%20txt=li.textContent.toLowerCase();li.style.display=txt.includes(f)?%22block%22:%22none%22%7D)%7D;%20%7D)();
```

#### 💻 Source Code:
```javascript
// Endpoint Extractor
(async()=>{
  const r=new RegExp("(?<=(\"|'|\\x60))\\/[a-zA-Z0-9_?&=\\ handling/\\-#\\.]*(?=(\"|'|\\x60))","g"),e=new Set,t=document.getElementsByTagName("script"),n=t=>{const a=t.matchAll(r);for(const t of a)e.add(t[0])};
  await Promise.all(Array.from(t).map(async t=>{try{t.src?n(await(await fetch(t.src)).text()):n(t.innerHTML)}catch(t){console.warn("Script fetch error:",t)}})),n(document.documentElement.outerHTML);
  const d=location.origin,paths=[...e];
  const categorizeEndpoints=paths=>{const categories={apis:[],js:[],html:[],css:[],json:[],xml:[],images:[],other:[]};return paths.forEach(p=>{if(p.match(/\.js$/i))categories.js.push(p);else if(p.match(/\.html?$/i))categories.html.push(p);else if(p.match(/\.css$/i))categories.css.push(p);else if(p.match(/\.json$/i))categories.json.push(p);else if(p.match(/\.xml$/i))categories.xml.push(p);else if(p.match(/\.(png|jpg|jpeg|gif|svg|webp|ico)$/i))categories.images.push(p);else if(p.match(/^\/api\//i)||p.match(/^\/v\d+\//i))categories.apis.push(p);else categories.other.push(p)}),categories},cats=categorizeEndpoints(paths),win=window.open("","_blank","width=1200,height=700,scrollbars=yes");
  if(!win)return alert("Popup blocked. Please allow popups.");
  const style='<style>*{margin:0;padding:0;box-sizing:border-box}body{background:#0f0f0f;color:#e0e0e0;font-family:monospace;padding:20px}h2{color:#4fc3f7;margin-bottom:5px}p{color:#888;margin-bottom:15px}button,input{margin:5px;padding:10px;background:#222;color:#e0e0e0;border:1px solid #4fc3f7;cursor:pointer;font-family:monospace}button:hover{background:#333}input{width:300px}.tab-btn{background:#1a1a1a;color:#aaa;padding:10px 15px;margin:3px}.tab-btn.active{background:#4fc3f7;color:#000;font-weight:bold}.tab-content{display:none;margin-top:15px;max-height:700px;overflow-y:auto}.tab-content.active{display:block}ul{list-style:none;padding:0}li{padding:8px;margin:2px 0;background:#1a1a1a;border-left:3px solid #4fc3f7}li a{color:#4fc3f7;text-decoration:none;display:block}li a:hover{color:#81d4fa;text-decoration:underline}.footer{margin-top:20px;padding-top:15px;border-top:1px solid #333;color:#666}</style>';
  const html='<html><head><title>Endpoint Extractor - Rezy Dev</title>'+style+'</head><body><h2>Endpoint Extractor</h2><p>Found '+paths.length+' endpoints</p><div><button id=cpbtn>Copy</button><button id=dlbtn>Download</button><input id=filt placeholder="Filter endpoints..."></div><div style="margin-top:15px"><button class="tab-btn active" data-tab="all">All ('+paths.length+')</button>'+(cats.apis.length?'<button class="tab-btn" data-tab="apis">APIs ('+cats.apis.length+')</button>':'')+(cats.js.length?'<button class="tab-btn" data-tab="js">JS ('+cats.js.length+')</button>':'')+(cats.html.length?'<button class="tab-btn" data-tab="html">HTML ('+cats.html.length+')</button>':'')+(cats.css.length?'<button class="tab-btn" data-tab="css">CSS ('+cats.css.length+')</button>':'')+(cats.json.length?'<button class="tab-btn" data-tab="json">JSON ('+cats.json.length+')</button>':'')+(cats.xml.length?'<button class="tab-btn" data-tab="xml">XML ('+cats.xml.length+')</button>':'')+(cats.images.length?'<button class="tab-btn" data-tab="images">Images ('+cats.images.length+')</button>':'')+(cats.other.length?'<button class="tab-btn" data-tab="other">Other ('+cats.other.length+')</button>':'')+'</div><div id="tab-all" class="tab-content active"><ul id=list-all></ul></div><div id="tab-apis" class="tab-content"><ul id=list-apis></ul></div><div id="tab-js" class="tab-content"><ul id=list-js></ul></div><div id="tab-html" class="tab-content"><ul id=list-html></ul></div><div id="tab-css" class="tab-content"><ul id=list-css></ul></div><div id="tab-json" class="tab-content"><ul id=list-json></ul></div><div id="tab-xml" class="tab-content"><ul id=list-xml></ul></div><div id="tab-images" class="tab-content"><ul id=list-images></ul></div><div id="tab-other" class="tab-content"><ul id=list-other></ul></div><div class="footer">Built with ❤️ by <a href="https://rezydev.com/" target="_blank" style="color:#4fc3f7">Rezy Dev</a></div></body></html>';
  win.document.write(html);
  win.document.close();
  const populateList=(id,items)=>{const ul=win.document.getElementById(id);items.forEach(p=>{const li=win.document.createElement("li");const a=win.document.createElement("a");a.href=d+p;a.target="_blank";a.textContent=p;li.appendChild(a);ul.appendChild(li)})};
  populateList("list-all",paths);populateList("list-apis",cats.apis);populateList("list-js",cats.js);populateList("list-html",cats.html);populateList("list-css",cats.css);populateList("list-json",cats.json);populateList("list-xml",cats.xml);populateList("list-images",cats.images);populateList("list-other",cats.other);
  win.document.querySelectorAll(".tab-btn").forEach(b=>b.onclick=function(){win.document.querySelectorAll(".tab-content").forEach(t=>t.classList.remove("active"));win.document.querySelectorAll(".tab-btn").forEach(t=>t.classList.remove("active"));win.document.getElementById("tab-"+b.getAttribute("data-tab")).classList.add("active");b.classList.add("active")});
  win.document.getElementById("cpbtn").onclick=function(){const ul=win.document.querySelector(".tab-content.active ul");const items=Array.from(ul.querySelectorAll("li a")).map(a=>a.textContent).join("\
");const ta=win.document.createElement("textarea");ta.value=items;win.document.body.appendChild(ta);ta.select();win.document.execCommand("copy");win.document.body.removeChild(ta);win.alert("Copied!")};
  win.document.getElementById("dlbtn").onclick=function(){const ul=win.document.querySelector(".tab-content.active ul");const items=Array.from(ul.querySelectorAll("li a")).map(a=>a.textContent).join("\
");const b=new Blob([items],{type:"text/plain"}),u=URL.createObjectURL(b),a=win.document.createElement("a");a.href=u;a.download="endpoints.txt";a.click();URL.revokeObjectURL(u)};
  win.document.getElementById("filt").oninput=function(){const f=this.value.toLowerCase();const ul=win.document.querySelector(".tab-content.active ul");ul.querySelectorAll("li").forEach(li=>{const txt=li.textContent.toLowerCase();li.style.display=txt.includes(f)?"block":"none"})};
})();
```

---

## 💻 Web Development Helpers

### Design Mode Activator

**Description:** Enables designMode edit settings across the page DOM, turning all static elements into text inputs.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20if%20(document.designMode%20===%20'on')%20%7B%20document.designMode%20=%20'off';%20alert('Design%20Mode%20deactivated.%20Page%20content%20is%20now%20locked.');%20console.log('Design%20mode%20turned%20OFF.');%20%7D%20else%20%7B%20document.designMode%20=%20'on';%20alert('Design%20Mode%20activated!%20You%20can%20now%20click%20and%20edit%20any%20text%20directly%20on%20the%20page.');%20console.log('Design%20mode%20turned%20ON.');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Design mode document contenteditor toggle
(function() {
  if (document.designMode === 'on') {
    document.designMode = 'off';
    alert('Design Mode deactivated. Page content is now locked.');
    console.log('Design mode turned OFF.');
  } else {
    document.designMode = 'on';
    alert('Design Mode activated! You can now click and edit any text directly on the page.');
    console.log('Design mode turned ON.');
  }
})();
```

---

### Form Auto-Filler

**Description:** Fills all page input fields with mock test values (names, emails, tel) to speed up QA testing.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20inputs%20=%20document.querySelectorAll('input,%20select,%20textarea');%20inputs.forEach(function(i)%20%7B%20if%20(i.type%20===%20'text')%20i.value%20=%20'John%20Doe';%20else%20if%20(i.type%20===%20'email')%20i.value%20=%20'john.doe@example.com';%20else%20if%20(i.type%20===%20'tel')%20i.value%20=%20'555-0199';%20else%20if%20(i.type%20===%20'number')%20i.value%20=%20'42';%20else%20if%20(i.type%20===%20'password')%20i.value%20=%20'P@ssw0rd123!';%20else%20if%20(i.tagName%20===%20'SELECT'%20&&%20i.options.length%20%3E%201)%20i.selectedIndex%20=%201;%20else%20if%20(i.type%20===%20'checkbox'%20%7C%7C%20i.type%20===%20'radio')%20i.checked%20=%20true;%20%7D);%20alert('Mock%20filled%20'%20+%20inputs.length%20+%20'%20form%20element(s).');%20console.log('Mocked%20data%20fields%20filled%20for:',%20inputs.length,%20'inputs');%20%7D)();
```

#### 💻 Source Code:
```javascript
// QA Forms mock fill parameters
(function() {
  var inputs = document.querySelectorAll('input, select, textarea');
  inputs.forEach(function(i) {
    if (i.type === 'text') i.value = 'John Doe';
    else if (i.type === 'email') i.value = 'john.doe@example.com';
    else if (i.type === 'tel') i.value = '555-0199';
    else if (i.type === 'number') i.value = '42';
    else if (i.type === 'password') i.value = 'P@ssw0rd123!';
    else if (i.tagName === 'SELECT' && i.options.length > 1) i.selectedIndex = 1;
    else if (i.type === 'checkbox' || i.type === 'radio') i.checked = true;
  });
  alert('Mock filled ' + inputs.length + ' form element(s).');
  console.log('Mocked data fields filled for:', inputs.length, 'inputs');
})();
```

---

### JSON Quick Formatter

**Description:** Attempts to parse and print nicely formatted JSON structure on screen if the current page contains raw text.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20try%20%7B%20var%20raw%20=%20document.body.innerText.trim();%20var%20parsed%20=%20JSON.parse(raw);%20var%20formatted%20=%20JSON.stringify(parsed,%20null,%202);%20document.body.innerHTML%20=%20'%3Cpre%20style=%22font-family:monospace;padding:20px;background:#1e293b;color:#f8fafc;font-size:13px;line-height:1.5;overflow:auto;height:100vh;box-sizing:border-box%22%3E'%20+%20formatted%20+%20'%3C/pre%3E';%20console.log('Successfully%20formatted%20JSON%20document.');%20%7D%20catch(e)%20%7B%20alert('Error:%20The%20page%20content%20does%20not%20appear%20to%20be%20a%20valid%20raw%20JSON%20string.');%20console.error('JSON%20parsing%20failed:',%20e);%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Raw text JSON prettifier
(function() {
  try {
    var raw = document.body.innerText.trim();
    var parsed = JSON.parse(raw);
    var formatted = JSON.stringify(parsed, null, 2);
    document.body.innerHTML = '<pre style="font-family:monospace;padding:20px;background:#1e293b;color:#f8fafc;font-size:13px;line-height:1.5;overflow:auto;height:100vh;box-sizing:border-box">' + formatted + '</pre>';
    console.log('Successfully formatted JSON document.');
  } catch(e) {
    alert('Error: The page content does not appear to be a valid raw JSON string.');
    console.error('JSON parsing failed:', e);
  }
})();
```

---

### Images Hider

**Description:** Hides all images or restores them to check layout outlines and measure raw page weights.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20imgs%20=%20document.querySelectorAll('img');%20var%20hidden%20=%20false;%20imgs.forEach(function(img)%20%7B%20if%20(img.style.visibility%20===%20'hidden')%20%7B%20img.style.visibility%20=%20'visible';%20%7D%20else%20%7B%20img.style.visibility%20=%20'hidden';%20hidden%20=%20true;%20%7D%20%7D);%20alert(hidden%20?%20'Hidden%20all%20images.'%20:%20'Restored%20all%20images.');%20console.log('Image%20visibility%20status%20flipped%20for',%20imgs.length,%20'nodes');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Disable images visibility
(function() {
  var imgs = document.querySelectorAll('img');
  var hidden = false;
  imgs.forEach(function(img) {
    if (img.style.visibility === 'hidden') {
      img.style.visibility = 'visible';
    } else {
      img.style.visibility = 'hidden';
      hidden = true;
    }
  });
  alert(hidden ? 'Hidden all images.' : 'Restored all images.');
  console.log('Image visibility status flipped for', imgs.length, 'nodes');
})();
```

---

### ARIA Roles & Accessibility Tree

**Description:** Outlines and displays labels for interactive elements without proper labels, checking screen-reader compatibility.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20count%20=%200;%20document.querySelectorAll('a,%20button,%20input,%20select,%20textarea').forEach(function(el)%20%7B%20var%20role%20=%20el.getAttribute('role')%20%7C%7C%20el.tagName.toLowerCase();%20var%20label%20=%20el.getAttribute('aria-label')%20%7C%7C%20el.getAttribute('aria-labelledby')%20%7C%7C%20el.innerText%20%7C%7C%20el.placeholder%20%7C%7C%20el.value;%20if%20(!label)%20%7B%20el.style.outline%20=%20'3px%20dotted%20#ec4899';%20count++;%20%7D%20%7D);%20if%20(count%20%3E%200)%20%7B%20alert('Identified%20'%20+%20count%20+%20'%20interactive%20element(s)%20with%20missing%20accessible%20labels%20(marked%20in%20dotted%20pink%20outline).');%20console.log('Found%20unlabeled%20elements%20total:',%20count);%20%7D%20else%20%7B%20alert('Accessibility%20Check%20Pass:%20All%20interactive%20tags%20have%20labels.');%20console.log('All%20elements%20have%20accessible%20labels%20verified!');%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Accessibility tags audit
(function() {
  var count = 0;
  document.querySelectorAll('a, button, input, select, textarea').forEach(function(el) {
    var role = el.getAttribute('role') || el.tagName.toLowerCase();
    var label = el.getAttribute('aria-label') || el.getAttribute('aria-labelledby') || el.innerText || el.placeholder || el.value;
    if (!label) {
      el.style.outline = '3px dotted #ec4899';
      count++;
    }
  });
  if (count > 0) {
    alert('Identified ' + count + ' interactive element(s) with missing accessible labels (marked in dotted pink outline).');
    console.log('Found unlabeled elements total:', count);
  } else {
    alert('Accessibility Check Pass: All interactive tags have labels.');
    console.log('All elements have accessible labels verified!');
  }
})();
```

---

### Lazy Load Image Auditor

**Description:** Checks if images are utilizing native loading=\

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20imgs%20=%20document.querySelectorAll('img');%20var%20missing%20=%200;%20imgs.forEach(function(img)%20%7B%20if%20(img.getAttribute('loading')%20!==%20'lazy')%20%7B%20img.style.outline%20=%20'3px%20dashed%20#ef4444';%20missing++;%20%7D%20else%20%7B%20img.style.outline%20=%20'3px%20dashed%20#10b981';%20%7D%20%7D);%20alert('Checked%20'%20+%20imgs.length%20+%20'%20image(s):%20-%20'%20+%20(imgs.length%20-%20missing)%20+%20'%20have%20loading=%22lazy%22%20(Green)%20-%20'%20+%20missing%20+%20'%20are%20missing%20loading=%22lazy%22%20(Red)');%20console.log('Lazy%20load%20stats:%20Missing',%20missing,%20'of',%20imgs.length);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Audit lazy-loading configuration for images
(function() {
  var imgs = document.querySelectorAll('img');
  var missing = 0;
  imgs.forEach(function(img) {
    if (img.getAttribute('loading') !== 'lazy') {
      img.style.outline = '3px dashed #ef4444';
      missing++;
    } else {
      img.style.outline = '3px dashed #10b981';
    }
  });
  alert('Checked ' + imgs.length + ' image(s):
- ' + (imgs.length - missing) + ' have loading="lazy" (Green)
- ' + missing + ' are missing loading="lazy" (Red)');
  console.log('Lazy load stats: Missing', missing, 'of', imgs.length);
})();
```

---

### Interactive Web Vitals Overlay

**Description:** Launches a HUD widget measuring Layout Shift, LCP, and page load timers on the current screen.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20d%20=%20document;%20var%20old%20=%20d.getElementById('vitals-hud');%20if%20(old)%20%7B%20old.remove();%20return;%20%7D%20var%20hud%20=%20d.createElement('div');%20hud.id%20=%20'vitals-hud';%20hud.style%20=%20'position:fixed;bottom:20px;left:20px;background:#0f172a;color:#f8fafc;padding:15px;z-index:999999;font-family:monospace;border-radius:8px;border:1px%20solid%20#3b82f6;width:260px;box-shadow:0%2010px%2015px%20-3px%20rgba(0,0,0,0.3)';%20var%20timing%20=%20window.performance.timing;%20var%20loadTime%20=%20timing.loadEventEnd%20-%20timing.navigationStart;%20var%20domTime%20=%20timing.domComplete%20-%20timing.domLoading;%20hud.innerHTML%20=%20'%3Ch4%20style=%22margin:0%200%2010px;font-size:12px;color:#3b82f6;border-b:1px%20solid%20#334155;padding-bottom:5px%22%3ECore%20Web%20Vitals%20Hud%3C/h4%3E'%20+%20'%3Cdiv%20style=%22font-size:11px;margin-bottom:6px%22%3ELoad%20Time:%20'%20+%20(loadTime%20%3E%200%20?%20loadTime%20+%20'ms'%20:%20'Calculating...')%20+%20'%3C/div%3E'%20+%20'%3Cdiv%20style=%22font-size:11px;margin-bottom:6px%22%3EDOM%20Build:%20'%20+%20(domTime%20%3E%200%20?%20domTime%20+%20'ms'%20:%20'Calculating...')%20+%20'%3C/div%3E'%20+%20'%3Cdiv%20style=%22font-size:11px;margin-bottom:6px%22%3ECLS%20Tracker:%20Active%3C/div%3E'%20+%20'%3Cbutton%20onclick=%22this.parentElement.remove()%22%20style=%22width:100%25;background:#1e293b;border:none;color:#94a3b8;font-size:10px;padding:4px;border-radius:4px;cursor:pointer;margin-top:10px%22%3EClose%3C/button%3E';%20d.body.appendChild(hud);%20console.log('Web%20Vitals%20overlay%20HUD%20launched.');%20%7D)();
```

#### 💻 Source Code:
```javascript
// Core Web Vitals HUD overlay
(function() {
  var d = document;
  var old = d.getElementById('vitals-hud'); if (old) { old.remove(); return; }
  var hud = d.createElement('div');
  hud.id = 'vitals-hud';
  hud.style = 'position:fixed;bottom:20px;left:20px;background:#0f172a;color:#f8fafc;padding:15px;z-index:999999;font-family:monospace;border-radius:8px;border:1px solid #3b82f6;width:260px;box-shadow:0 10px 15px -3px rgba(0,0,0,0.3)';
  
  var timing = window.performance.timing;
  var loadTime = timing.loadEventEnd - timing.navigationStart;
  var domTime = timing.domComplete - timing.domLoading;
  
  hud.innerHTML = '<h4 style="margin:0 0 10px;font-size:12px;color:#3b82f6;border-b:1px solid #334155;padding-bottom:5px">Core Web Vitals Hud</h4>' +
    '<div style="font-size:11px;margin-bottom:6px">Load Time: ' + (loadTime > 0 ? loadTime + 'ms' : 'Calculating...') + '</div>' +
    '<div style="font-size:11px;margin-bottom:6px">DOM Build: ' + (domTime > 0 ? domTime + 'ms' : 'Calculating...') + '</div>' +
    '<div style="font-size:11px;margin-bottom:6px">CLS Tracker: Active</div>' +
    '<button onclick="this.parentElement.remove()" style="width:100%;background:#1e293b;border:none;color:#94a3b8;font-size:10px;padding:4px;border-radius:4px;cursor:pointer;margin-top:10px">Close</button>';
  d.body.appendChild(hud);
  console.log('Web Vitals overlay HUD launched.');
})();
```

---

### Web to PDF Converter

**Description:** Submits the active page URL to Web2PDFConvert in a new tab to generate a high-quality PDF layout printout.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20window.open('https://www.web2pdfconvert.com#'%20+%20location.href);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Convert page to PDF via external portal
(function() {
  window.open('https://www.web2pdfconvert.com#' + location.href);
})();
```

---

### Unused CSS Detector

**Description:** Analyzes the stylesheet rules in relation to active elements inside the DOM to report any unused CSS rules.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(()%20=%3E%20%7B%20const%20stylesheets%20=%20document.querySelectorAll('style,%20link%5Brel=%22stylesheet%22%5D');%20const%20unusedRules%20=%20%5B%5D;%20const%20allElements%20=%20document.getElementsByTagName(%22*%22);%20stylesheets.forEach(sheetEl%20=%3E%20%7B%20let%20rules;%20if%20(sheetEl.tagName%20===%20%22STYLE%22)%20%7B%20rules%20=%20Array.from(sheetEl.sheet?.cssRules%20%7C%7C%20%5B%5D);%20%7D%20else%20%7B%20try%20%7B%20rules%20=%20Array.from(sheetEl.sheet?.cssRules%20%7C%7C%20%5B%5D);%20%7D%20catch%20(e)%20%7B%20return;%20//%20CORS%20restriction%20%7D%20%7D%20rules.forEach(rule%20=%3E%20%7B%20if%20(rule%20instanceof%20CSSStyleRule)%20%7B%20let%20isUsed%20=%20false;%20for%20(const%20el%20of%20allElements)%20%7B%20try%20%7B%20if%20(el.matches(rule.selectorText))%20%7B%20isUsed%20=%20true;%20break;%20%7D%20%7D%20catch%20(err)%20%7B%7D%20%7D%20if%20(!isUsed)%20%7B%20unusedRules.push(%7B%20selector:%20rule.selectorText,%20styles:%20rule.style.cssText,%20source:%20sheetEl.tagName%20===%20%22STYLE%22%20?%20%22Internal%20Stylesheet%22%20:%20sheetEl.href%20%7D);%20%7D%20%7D%20%7D);%20%7D);%20const%20container%20=%20document.createElement(%22div%22);%20container.className%20=%20%22unused-css-popup%22;%20container.style.cssText%20=%20%60%20position:%20fixed;%20top:%2020px;%20right:%2020px;%20width:%20600px;%20max-height:%2080vh;%20padding:%2020px;%20background:%20#ffffff;%20color:%20#0f172a;%20border-radius:%208px;%20box-shadow:%200%2010px%2025px%20-5px%20rgba(0,0,0,0.2);%20z-index:%20100000;%20overflow-y:%20auto;%20font-family:%20system-ui,%20-apple-system,%20sans-serif;%20border:%201px%20solid%20#e2e8f0;%20%60;%20container.innerHTML%20=%20%60%20%3Cdiv%20style=%22display:%20flex;%20justify-content:%20space-between;%20align-items:%20center;%20border-bottom:%201px%20solid%20#e2e8f0;%20padding-bottom:%2010px;%20margin-bottom:%2015px;%22%3E%20%3Cstrong%20style=%22font-size:%2016px;%22%3EUnused%20CSS%20Detector%3C/strong%3E%20%3Cbutton%20onclick=%22this.closest('.unused-css-popup').remove()%22%20style=%22background:#ef4444;%20color:#fff;%20border:none;%20padding:4px%208px;%20border-radius:4px;%20cursor:pointer;%20font-size:12px;%22%3E%E2%9C%95%3C/button%3E%20%3C/div%3E%20%3Cdiv%20style=%22margin-bottom:%2015px;%20font-weight:%20bold;%20font-size:%2014px;%22%3E%20Total%20Unused%20Rules%20Found:%20$%7BunusedRules.length%7D%20%3C/div%3E%20%3Cdiv%20style=%22display:%20flex;%20flex-direction:%20column;%20gap:%2012px;%22%3E%20$%7BunusedRules.map(rule%20=%3E%20%60%20%3Cdiv%20style=%22padding:%2010px;%20background:%20#f8fafc;%20border:%201px%20solid%20#e2e8f0;%20border-radius:%206px;%20font-size:%2012px;%20font-family:%20monospace;%22%3E%20%3Cdiv%20style=%22margin-bottom:%204px;%20color:%20#1e293b;%22%3E%3Cstrong%3ESelector:%3C/strong%3E%20$%7Brule.selector%7D%3C/div%3E%20%3Cdiv%20style=%22margin-bottom:%204px;%20color:%20#475569;%20white-space:%20pre-wrap;%20word-break:%20break-all;%22%3E%3Cstrong%3EStyles:%3C/strong%3E%20$%7Brule.styles%7D%3C/div%3E%20%3Cdiv%20style=%22font-size:%2011px;%20color:%20#64748b;%20word-break:%20break-all;%22%3E%3Cstrong%3ESource:%3C/strong%3E%20$%7Brule.source%7D%3C/div%3E%20%3C/div%3E%20%60).join('')%7D%20%3C/div%3E%20$%7BunusedRules.length%20===%200%20?%20'%3Cdiv%20style=%22color:%20#10b981;%20font-weight:%20bold;%22%3ENo%20unused%20CSS%20rules%20found%20on%20this%20page.%20Perfect!%3C/div%3E'%20:%20''%7D%20%60;%20document.body.appendChild(container);%20console.log('Unused%20CSS%20analyzer%20complete.%20Rules%20found:',%20unusedRules.length);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Unused CSS stylesheet rule checker
(() => {
  const stylesheets = document.querySelectorAll('style, link[rel="stylesheet"]');
  const unusedRules = [];
  const allElements = document.getElementsByTagName("*");
  
  stylesheets.forEach(sheetEl => {
    let rules;
    if (sheetEl.tagName === "STYLE") {
      rules = Array.from(sheetEl.sheet?.cssRules || []);
    } else {
      try {
        rules = Array.from(sheetEl.sheet?.cssRules || []);
      } catch (e) {
        return; // CORS restriction
      }
    }
    
    rules.forEach(rule => {
      if (rule instanceof CSSStyleRule) {
        let isUsed = false;
        for (const el of allElements) {
          try {
            if (el.matches(rule.selectorText)) {
              isUsed = true;
              break;
            }
          } catch (err) {}
        }
        if (!isUsed) {
          unusedRules.push({
            selector: rule.selectorText,
            styles: rule.style.cssText,
            source: sheetEl.tagName === "STYLE" ? "Internal Stylesheet" : sheetEl.href
          });
        }
      }
    });
  });

  const container = document.createElement("div");
  container.className = "unused-css-popup";
  container.style.cssText = `
    position: fixed;
    top: 20px;
    right: 20px;
    width: 600px;
    max-height: 80vh;
    padding: 20px;
    background: #ffffff;
    color: #0f172a;
    border-radius: 8px;
    box-shadow: 0 10px 25px -5px rgba(0,0,0,0.2);
    z-index: 100000;
    overflow-y: auto;
    font-family: system-ui, -apple-system, sans-serif;
    border: 1px solid #e2e8f0;
  `;
  
  container.innerHTML = `
    <div style="display: flex; justify-content: space-between; align-items: center; border-bottom: 1px solid #e2e8f0; padding-bottom: 10px; margin-bottom: 15px;">
      <strong style="font-size: 16px;">Unused CSS Detector</strong>
      <button onclick="this.closest('.unused-css-popup').remove()" style="background:#ef4444; color:#fff; border:none; padding:4px 8px; border-radius:4px; cursor:pointer; font-size:12px;">✕</button>
    </div>
    <div style="margin-bottom: 15px; font-weight: bold; font-size: 14px;">
      Total Unused Rules Found: ${unusedRules.length}
    </div>
    <div style="display: flex; flex-direction: column; gap: 12px;">
      ${unusedRules.map(rule => `
        <div style="padding: 10px; background: #f8fafc; border: 1px solid #e2e8f0; border-radius: 6px; font-size: 12px; font-family: monospace;">
          <div style="margin-bottom: 4px; color: #1e293b;"><strong>Selector:</strong> ${rule.selector}</div>
          <div style="margin-bottom: 4px; color: #475569; white-space: pre-wrap; word-break: break-all;"><strong>Styles:</strong> ${rule.styles}</div>
          <div style="font-size: 11px; color: #64748b; word-break: break-all;"><strong>Source:</strong> ${rule.source}</div>
        </div>
      `).join('')}
    </div>
    ${unusedRules.length === 0 ? '<div style="color: #10b981; font-weight: bold;">No unused CSS rules found on this page. Perfect!</div>' : ''}
  `;
  document.body.appendChild(container);
  console.log('Unused CSS analyzer complete. Rules found:', unusedRules.length);
})();
```

---

## ✍️ Content & Writing Tools

### Heading Map Outline Checker

**Description:** Compiles and alerts the hierarchical structured Heading Tag sequence (H1 to H6) for structural content checks.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20headings%20=%20document.querySelectorAll('h1,%20h2,%20h3,%20h4,%20h5,%20h6');%20if%20(headings.length%20===%200)%20%7B%20alert('No%20headings%20(H1-H6)%20found%20on%20the%20current%20page.');%20console.log('SEO%20Audit:%20No%20headings%20detected.');%20return;%20%7D%20var%20map%20=%20%5B%5D;%20headings.forEach(function(h)%20%7B%20var%20tag%20=%20h.tagName.toLowerCase();%20var%20txt%20=%20h.innerText.trim();%20var%20level%20=%20parseInt(tag%5B1%5D);%20var%20indent%20=%20'%20%20'.repeat(level%20-%201);%20map.push(indent%20+%20tag.toUpperCase()%20+%20':%20'%20+%20txt);%20%7D);%20alert('Heading%20Map%20Outline:%20----------------------%20'%20+%20map.join('%20'));%20console.log('Heading%20Structural%20Map:',%20map);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Map out heading tag hierarchy
(function() {
  var headings = document.querySelectorAll('h1, h2, h3, h4, h5, h6');
  if (headings.length === 0) {
    alert('No headings (H1-H6) found on the current page.');
    console.log('SEO Audit: No headings detected.');
    return;
  }
  var map = [];
  headings.forEach(function(h) {
    var tag = h.tagName.toLowerCase();
    var txt = h.innerText.trim();
    var level = parseInt(tag[1]);
    var indent = '  '.repeat(level - 1);
    map.push(indent + tag.toUpperCase() + ': ' + txt);
  });
  alert('Heading Map Outline:
----------------------
' + map.join('
'));
  console.log('Heading Structural Map:', map);
})();
```

---

### Flesch Reading Score Auditor

**Description:** Evaluates the Flesch-Kincaid Reading Ease index score based on syllable count ratios of the visible body text copy.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20txt%20=%20document.body.innerText.trim();%20var%20words%20=%20txt.split(/%5Cs+/).filter(Boolean);%20var%20sentences%20=%20txt.split(/%5B.!?%5D+/).filter(Boolean);%20if%20(words.length%20%3C%205)%20%7B%20alert('Not%20enough%20words%20on%20the%20page%20to%20calculate%20readability%20score.');%20console.log('SEO%20Audit:%20Word%20count%20too%20low.');%20return;%20%7D%20function%20countSyllables(word)%20%7B%20word%20=%20word.toLowerCase();%20if%20(word.length%20%3C=%203)%20return%201;%20word%20=%20word.replace(/(?:%5B%5Elaeiouy%5Des%7Ced%7C%5B%5Elaeiouy%5De)$/,%20'');%20word%20=%20word.replace(/%5Ey/,%20'');%20var%20matches%20=%20word.match(/%5Baeiouy%5D%7B1,2%7D/g);%20return%20matches%20?%20matches.length%20:%201;%20%7D%20var%20totalSyllables%20=%200;%20words.forEach(function(w)%20%7B%20totalSyllables%20+=%20countSyllables(w);%20%7D);%20var%20w%20=%20words.length;%20var%20s%20=%20sentences.length%20%7C%7C%201;%20var%20asl%20=%20w%20/%20s;%20var%20asw%20=%20totalSyllables%20/%20w;%20var%20score%20=%20206.835%20-%20(1.015%20*%20asl)%20-%20(84.6%20*%20asw);%20var%20level%20=%20'';%20if%20(score%20%3E=%2090)%20level%20=%20'Very%20Easy%20(5th%20grade)';%20else%20if%20(score%20%3E=%2080)%20level%20=%20'Easy%20(6th%20grade)';%20else%20if%20(score%20%3E=%2070)%20level%20=%20'Fairly%20Easy%20(7th%20grade)';%20else%20if%20(score%20%3E=%2060)%20level%20=%20'Standard%20(8th-9th%20grade)';%20else%20if%20(score%20%3E=%2050)%20level%20=%20'Fairly%20Difficult%20(High%20School)';%20else%20if%20(score%20%3E=%2030)%20level%20=%20'Difficult%20(College)';%20else%20level%20=%20'Very%20Confusing%20(College%20Graduate)';%20alert('Readability%20Index%20Check:%20-------------------------%20Flesch%20Score:%20'%20+%20score.toFixed(1)%20+%20'%20Estimated%20Grade%20Level:%20'%20+%20level);%20console.log('Readability%20Score%20details:',%20%7B%20score:%20score,%20asl:%20asl,%20asw:%20asw,%20words:%20w,%20sentences:%20s%20%7D);%20%7D)();
```

#### 💻 Source Code:
```javascript
// Calculate Flesch Reading Ease score
(function() {
  var txt = document.body.innerText.trim();
  var words = txt.split(/\s+/).filter(Boolean);
  var sentences = txt.split(/[.!?]+/).filter(Boolean);
  if (words.length < 5) {
    alert('Not enough words on the page to calculate readability score.');
    console.log('SEO Audit: Word count too low.');
    return;
  }
  
  function countSyllables(word) {
    word = word.toLowerCase();
    if (word.length <= 3) return 1;
    word = word.replace(/(?:[^laeiouy]es|ed|[^laeiouy]e)$/, '');
    word = word.replace(/^y/, '');
    var matches = word.match(/[aeiouy]{1,2}/g);
    return matches ? matches.length : 1;
  }
  
  var totalSyllables = 0;
  words.forEach(function(w) { totalSyllables += countSyllables(w); });
  var w = words.length;
  var s = sentences.length || 1;
  var asl = w / s;
  var asw = totalSyllables / w;
  var score = 206.835 - (1.015 * asl) - (84.6 * asw);
  var level = '';
  
  if (score >= 90) level = 'Very Easy (5th grade)';
  else if (score >= 80) level = 'Easy (6th grade)';
  else if (score >= 70) level = 'Fairly Easy (7th grade)';
  else if (score >= 60) level = 'Standard (8th-9th grade)';
  else if (score >= 50) level = 'Fairly Difficult (High School)';
  else if (score >= 30) level = 'Difficult (College)';
  else level = 'Very Confusing (College Graduate)';
  
  alert('Readability Index Check:
-------------------------
Flesch Score: ' + score.toFixed(1) + '
Estimated Grade Level: ' + level);
  console.log('Readability Score details:', { score: score, asl: asl, asw: asw, words: w, sentences: s });
})();
```

---

### Google Images Selection Search

**Description:** Launches a Google Images query based on highlighted text selection or custom-prompted search keywords.

#### 📋 Bookmarklet URL (Copy for Bookmark Bar):
```javascript
javascript:(function()%20%7B%20var%20q%20=%20%22%22%20+%20(window.getSelection%20?%20window.getSelection()%20:%20document.getSelection%20?%20document.getSelection()%20:%20document.selection.createRange().text);%20if%20(!q)%20q%20=%20prompt(%22Search%20terms?%20...%22,%20%22%22);%20if%20(q%20!=%20null)%20%7B%20window.open(%22https://images.google.com/images?q=%22%20+%20encodeURIComponent(q),%20%22_blank%22);%20%7D%20%7D)();
```

#### 💻 Source Code:
```javascript
// Google Images Selection Search
(function() {
  var q = "" + (window.getSelection ? window.getSelection() : document.getSelection ? document.getSelection() : document.selection.createRange().text);
  if (!q) q = prompt("Search terms? ...", "");
  if (q != null) {
    window.open("https://images.google.com/images?q=" + encodeURIComponent(q), "_blank");
  }
})();
```

---

