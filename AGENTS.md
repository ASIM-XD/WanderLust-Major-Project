# Wanderlust UI Design Guidelines

## State-of-the-Art Aesthetics
When creating or modifying the UI for the Wanderlust application (EJS templates and CSS), you MUST adhere to the following premium design principles:

1. **Rich Aesthetics**: 
   - Avoid basic or generic colors (like plain red `#FF0000` or blue `#0000FF`).
   - Use curated, harmonious color palettes (e.g., modern dark modes, sleek minimalist light modes, and vibrant accent colors).
   - Implement modern UI trends like glassmorphism (translucent backgrounds with blur), subtle gradients, and soft drop-shadows where appropriate.

2. **Modern Typography**:
   - Never use browser default fonts.
   - Always import and use modern fonts from Google Fonts (e.g., 'Inter', 'Outfit', 'Poppins', or 'Roboto').
   - Maintain clear visual hierarchy using appropriate font weights, sizes, and letter spacing.

3. **Dynamic Interactions & Micro-animations**:
   - The interface must feel alive and responsive.
   - Add smooth transitions (`transition: all 0.3s ease;`) to interactive elements.
   - Include hover effects for buttons, cards, and links (e.g., slight scaling `transform: scale(1.02)`, shadow elevation, or color shifts).

4. **Premium Layouts**:
   - Ensure all layouts are fully responsive.
   - Use CSS Flexbox and Grid to create clean, aligned, and spacious designs.
   - Maintain generous padding and margins to let the content breathe.

5. **Vanilla CSS Focus**:
   - Prioritize Vanilla CSS for styling to maintain maximum control and flexibility over the design.

**CRITICAL RULE**: If your design looks simple, generic, or like a basic MVP, you have failed. The user should be WOWED at first glance.
