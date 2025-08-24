# Product Requirements Document (PRD)
## Matchaboy POS System - Mini Cashier Application

### 🏢 Business Information
- **Name**: Matchaboy - Wanayasa
- **Address**: Jl. Wanayasa, Purwakarta, Jawa Barat
- **Instagram**: @matchaboy
- **Tagline**: "The best Matcha here"

### 🎨 Design Theme
**Primary Brand Color**: Matcha Green
- **Primary Green**: `#4A7C59` (Deep matcha green)
- **Light Green**: `#7FB069` (Fresh matcha)
- **Accent Green**: `#A7D7C5` (Soft mint)
- **Background Green**: `#F0F7F4` (Very light mint)
- **Dark Green**: `#2D5016` (Text/headers)
- **Warm Accent**: `#D4A574` (Complementary brown for highlights)

---

## 🍵 Product Menu

### **Drinks Category** (Primary Focus)
| Product Name | Price | Category |
|--------------|-------|----------|
| Matcha Latte | Rp13.000 | Drink |
| Cloud Matcha | Rp15.000 | Drink |
| Matcha Cookies | Rp15.000 | Drink |
| Coconut Matcha | Rp15.000 | Drink |
| Honey Matcha | Rp13.000 | Drink |
| Strawberry Cream Matcha | Rp15.000 | Drink |
| Caramel Matcha | Rp15.000 | Drink |
| Ubi Cream Matcha Latte | Rp15.000 | Drink |
| Choco Cream Matcha | Rp15.000 | Drink |

### **Snacks Category** (Additional Items)
*To be defined based on future menu expansion*

---

## 📋 Core Features & Requirements

### 1. **New Order Management**

#### 1.1 Product Selection Interface
- **Product Display**: 
  - Grid layout with product images and titles
  - Large, touch-friendly product cards (minimum 120px height)
  - Clear pricing visible on each card
  - **Drinks Section**: Prominent 3x3 or 3x4 grid for all matcha beverages
  - **Product Card Design**: Matcha-themed with green gradients
- **Categories**:
  - **Primary**: Drinks (9 matcha beverages - main focus)
  - **Secondary**: Snacks (expandable section for future items)
- **Product Information**:
  - High-quality matcha product images (placeholder support for now)
  - Product name prominently displayed in readable font
  - Price clearly visible with Rupiah formatting
  - Quick quantity adjustment (+/- buttons)
  - Visual feedback for selected items

#### 1.2 Order Composition
- **Real-time Total**: Live calculation and display of order total
- **Order Summary Panel**: Shows selected items with quantities and subtotals
- **Customer Name**: Optional field, non-blocking to order flow
- **Price Range Display**: Show that most drinks are Rp13.000-15.000 range
- **Quick Actions**: Clear order, modify quantities

#### 1.3 Payment Processing
- **Payment Amount Input**: 
  - Quick denomination buttons: **Rp15.000**, **Rp20.000**, **Rp25.000**, **Rp50.000**, **Rp100.000**
  - **Smart Suggestions**: Auto-suggest amounts based on order total (e.g., if total is Rp13.000, highlight Rp15.000)
  - Custom amount input field
  - Auto-calculate change with clear display
- **Change Calculation**: 
  - Real-time change display
  - Warning if payment insufficient
  - Clear visual feedback for exact payment
  - Handle common scenarios (single drink orders, multiple items)

#### 1.4 Receipt & Completion
- **Print Receipt**: One-click receipt printing with Matchaboy branding
- **Order Completion**: Clear completion status
- **Next Order**: Quick reset for new customer

### 2. **Order Monitoring System**

#### 2.1 Processing Queue
- **Visual Order Queue**: List of orders being prepared
- **Order Status Indicators**:
  - 🟡 New Order (just placed)
  - 🔵 In Progress (being prepared)
  - 🟢 Ready (ready for pickup)
  - ⚪ Completed (handed to customer)
- **Time Tracking**: Order creation timestamp
- **Customer Information**: Order number and customer name (if provided)
- **Order Contents**: Quick view of items in each order

#### 2.2 Order Management Actions
- **Status Updates**: Mark as in-progress, ready, completed
- **Order Details**: View full order contents with quantities
- **Priority Management**: Ability to prioritize urgent orders
- **Order Cancellation**: Cancel orders if needed with reason

### 3. **User Experience Design**

#### 3.1 Layout Strategy
**Recommended Layout**: Split-screen approach optimized for matcha shop workflow
- **Left Panel (65%)**: New Order Interface
  - **Drinks Grid**: 3-column grid showcasing all 9 matcha drinks
  - **Order Summary**: Collapsible/expandable order details
  - **Payment Section**: Prominent with smart denomination suggestions
- **Right Panel (35%)**: Order Monitoring
  - **Processing Queue**: Vertical list of active orders
  - **Order Status Management**: Quick status update buttons
  - **Queue Statistics**: Orders pending, ready, etc.

#### 3.2 Mobile Responsiveness
- **Tablet Mode**: Side-by-side panels (recommended for cashier use)
- **Mobile Mode**: Tabbed interface (New Order / Monitor Orders)
- **Touch Optimization**: Large buttons (min 44px), swipe gestures

### 4. **Technical Requirements**

#### 4.1 Data Persistence
- **Local Storage**: 
  - All order data and history
  - Product information (prices, names, availability)
  - User settings and preferences
- **Order History**: Keep completed orders for the day/session
- **Settings Persistence**: Theme, printer settings, custom denominations

#### 4.2 Printer Integration
- **Connection Persistence**: Remember connected printer across browser refreshes
- **Auto-reconnect**: Attempt to reconnect on app load
- **Connection Status**: Always visible printer status indicator
- **Receipt Format**: Optimized for thermal printer with Matchaboy branding

#### 4.3 Performance
- **Fast Loading**: Quick app initialization with cached product data
- **Smooth Interactions**: No lag in UI updates, especially order total calculation
- **Reliable Printing**: Robust error handling for print failures

---

## 🎯 User Journey Flow

### Primary Cashier Workflow:
1. **App Loads** → View split-screen with 9 matcha drinks displayed
2. **Customer Orders** → "Satu Cloud Matcha dan satu Honey Matcha"
3. **Select Products** → Tap Cloud Matcha (+), Honey Matcha (+)
4. **View Total** → See Rp28.000 total instantly
5. **Enter Payment** → Customer pays Rp30.000 (tap Rp30.000 or custom)
6. **Show Change** → Display Rp2.000 change due
7. **Print Receipt** → One-click print with Matchaboy header
8. **Monitor Preparation** → Order appears in right panel queue
9. **Update Status** → Mark "In Progress" → "Ready" → "Completed"
10. **Next Customer** → Interface ready for new order

### Typical Order Scenarios:
- **Single Drink**: Customer orders 1x Matcha Latte (Rp13.000) → pays Rp15.000 → Rp2.000 change
- **Multiple Same**: Customer orders 2x Cloud Matcha (Rp30.000) → pays Rp50.000 → Rp20.000 change
- **Mixed Order**: Customer orders 1x Honey Matcha + 1x Choco Cream Matcha (Rp28.000) → exact payment

---

## 🔧 Additional Features to Consider

### Nice-to-Have Features:
1. **Daily Sales Summary**: Track which matcha drinks sell most
2. **Product Availability**: Mark items as "sold out" during day
3. **Customer Favorites**: Track popular combinations
4. **Rush Hour Mode**: Simplified interface for busy periods
5. **Price Adjustments**: Temporary promotions or discounts
6. **Order Notes**: Special requests (less sweet, extra ice, etc.)
7. **Receipt Customization**: Add Instagram handle, promotions

### Future Product Expansion:
1. **Seasonal Drinks**: Limited time matcha variations
2. **Snack Items**: Matcha cookies, cakes, pastries
3. **Size Options**: Regular/Large sizes for drinks
4. **Hot/Cold Options**: Temperature variants for drinks
5. **Add-ons**: Extra matcha shot, different milk types

---

## 📱 Interface Priorities for Matcha Shop

### Critical UX Elements:
1. **Speed**: Quick selection from 9 drink options
2. **Visual Appeal**: Green theme reinforces matcha brand
3. **Price Clarity**: Clear Rp13k-15k pricing visible
4. **Touch-Friendly**: Easy tapping for busy cashiers
5. **Error Prevention**: Prevent wrong orders/payments
6. **Brand Consistency**: Matchaboy identity throughout

### Success Metrics:
- Average order time: < 90 seconds (simple matcha shop orders)
- Payment accuracy: 100% correct change calculation
- Order accuracy: Zero wrong drink preparations
- Customer satisfaction: Clear receipts with Instagram handle
- Peak hour performance: Handle 3-4 orders simultaneously

### Matcha-Specific Considerations:
- **Product Photography**: High-quality matcha drink images essential
- **Green Theme Consistency**: All UI elements reflect matcha branding
- **Price Point**: Most items Rp15k - optimize payment flow for this
- **Order Complexity**: Generally simple orders (1-2 drinks per customer)
- **Brand Promotion**: Include @matchaboy Instagram on all touchpoints

---

## 📊 Data Models

### Order Data Structure
```javascript
{
  id: "order_20250824_001",
  timestamp: "2025-08-24T10:30:00Z",
  customerName: "John Doe",
  items: [
    {
      productId: "cloud_matcha",
      productName: "Cloud Matcha",
      price: 15000,
      quantity: 2
    }
  ],
  subtotal: 30000,
  tax: 0,
  total: 30000,
  payment: {
    amount: 50000,
    change: 20000
  },
  status: "new", // new, in_progress, ready, completed, cancelled
  notes: ""
}
```

### Product Data Structure
```javascript
{
  id: "cloud_matcha",
  name: "Cloud Matcha",
  category: "drinks",
  price: 15000,
  image: "/images/cloud-matcha.jpg",
  available: true,
  description: "Creamy matcha with cloud-like foam"
}
```

---

## 🚀 Development Phases

### Phase 1: Core POS Functionality
- [ ] Product grid display
- [ ] Order management
- [ ] Payment calculation
- [ ] Basic receipt printing
- [ ] Local data storage

### Phase 2: Order Queue Management
- [ ] Order status tracking
- [ ] Queue display
- [ ] Status updates
- [ ] Time tracking

### Phase 3: Enhanced Features
- [ ] Smart payment suggestions
- [ ] Customer name handling
- [ ] Order notes
- [ ] Daily summaries

### Phase 4: Polish & Optimization
- [ ] Performance optimization
- [ ] Advanced printer features
- [ ] Error handling
- [ ] User experience refinements

---

This comprehensive PRD in markdown format provides a complete blueprint for developing the Matchaboy POS system with all specified requirements, product menu, and technical considerations.