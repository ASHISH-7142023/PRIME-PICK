# PRIME•PICK 🛍️

A premium, responsive, frontend-only multi-page e-commerce storefront for fashion and garments. Designed with modern web standards, Prime Pick offers an interactive shopping catalog, dynamic live-filtering search, and a simulated checkout flow, all driven by client-side interactions.

---

## 🚀 Tech Stack

Prime Pick is built purely with frontend technologies for maximum speed, simplicity, and ease of local testing.

- **HTML5**: Structured semantic markup for all page templates.
- **Vanilla CSS3**: 
  - Modern responsive layouts with Flexbox and Grid.
  - Curated, premium dark/light color palette (using modern HSL-style styling, sleek dark-themed overlays, and clean grey backgrounds).
  - Custom scrollbar hiding and fluid transitions (`all ease-in-out`).
  - Immersive CSS keyframe animations (such as the rotating `boing` interaction on inputs).
- **jQuery (CDN)**:
  - Cursor tracking algorithms (magnifying mouse circle `.custom` overlay).
  - Live local catalog search and table-row text filtering.
  - Simulated shopping cart: dynamic element cloning, cart badge/ping notification, and reactive item removal.
- **Remix Icon & SVG**: Crisp, modern iconography for navbar links, shopping cart buttons, and social media handles in the footer.

---

## 📂 Project Structure & Path Map

Below is a breakdown of the repository's files and their respective purposes:

```mermaid
graph TD
    index.html --> shopnow.html
    index.html --> searchTable.html
    searchTable.html --> thankYou.html
    
    style.css -.-> index.html
    style.css -.-> thankYou.html
    styleforShopnow.css -.-> shopnow.html
    styleSearch.css -.-> searchTable.html
```

### 📄 Pages (HTML)
*   **[index.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/index.html)**: The homepage. Introduces the brand, presents a call-to-action (CTA) to "Shop Now", features a custom mouse follower circle, and hosts the global site navbar and footer.
*   **[shopnow.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/shopnow.html)**: The product catalog page. Showcases a visual grid of garments (jackets, hoodies, dresses, shirts) with prices and custom overlay styles.
*   **[searchTable.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/searchTable.html)**: The interactive search and cart workspace. Features a table containing all products, search input with dynamic character-filtering, and an append-cloned Cart slide-out drawer.
*   **[thankYou.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/thankYou.html)**: Order confirmation screen displayed post-checkout.

### 🎨 Stylesheets (CSS)
*   **[style.css](file:///d:/ASHISH%20GITHUB/PRIME-PICK/style.css)**: Core style declarations. Defines font families (Montserrat, Geologica, Sometype Mono), global reset parameters, custom circular mouse tracker `.custom`, and footer configurations.
*   **[styleforShopnow.css](file:///d:/ASHISH%20GITHUB/PRIME-PICK/styleforShopnow.css)**: Layout styling specific to the shop grid gallery (`.shopnow-page`, product `.item` cards, price badges).
*   **[styleSearch.css](file:///d:/ASHISH%20GITHUB/PRIME-PICK/styleSearch.css)**: CSS declarations for the tabular catalog representation, slide-out checkout sidebar (`.cart-div`), and cart notification badge (`.cart-ping`).

---

## 🔄 Core Workflows

### 1. Browse & Discovery Workflow
1. The user lands on **Home** ([index.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/index.html)).
2. An interactive, smooth circle tracker (`.custom`) follows the cursor using mouse coordinates.
3. Clicking **Shop Now** or selecting **Shop** from the header directs the user to the Catalog page ([shopnow.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/shopnow.html)).

### 2. Live Search & Filter Workflow
1. Clicking on the **Search for Products** input on the Home or Catalog page instantly redirects the user to the Search Workspace ([searchTable.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/searchTable.html)).
2. As the user types query terms in the search field:
   - A jQuery keyup event captures the input string.
   - Rows (`tr`) within the product table body (`tbody`) are filtered using jQuery's `.filter()` method.
   - Rows not matching the search query are faded/hidden instantly without page reloads.

### 3. Cart & Simulated Checkout Workflow
1. In the Search Workspace, clicking **Add to Cart** on a product triggers a series of interactive states:
   - The button text toggles to **Remove** and updates to a red styling highlight.
   - The red cart notification dot (`.cart-ping`) appears on the navbar cart icon.
   - The matching product card element is cloned and prepended to the slide-out checkout sidebar (`.cart-div`).
2. Clicking the cart icon in the navbar toggles the visibility of `.cart-div` by adding/removing the `.cart-appear` class.
3. Within the sidebar, clicking an item deletes the element from the cart and resets the catalog item's button back to "Add to Cart".
4. Clicking the **Checkout** button redirects the user to the confirmation page ([thankYou.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/thankYou.html)).

---

## 🛠️ Local Development & Execution

Since the project has no backend server or package dependencies, running it is simple:

1. Clone or download the workspace directory.
2. Launch a local static server (e.g., using VS Code Live Server extension or `python -m http.server 8000`).
3. Alternatively, double-click **[index.html](file:///d:/ASHISH%20GITHUB/PRIME-PICK/index.html)** to open the application directly in any modern web browser.