# ☕ Coffee Shop Sales Dashboard

A comprehensive Power BI dashboard analyzing coffee shop transaction data with interactive visualizations and key performance indicators.

This dashboard provides insights into:
- **Total Sales**: 698.81K
- **Average Order Value**: 4.69
- **Total Orders**: 149K
- **Total Items Sold**: 214K

## 🎯 Key Features

### KPI Cards
- Real-time sales metrics
- Order performance indicators
- Customer behavior insights

### Interactive Visualizations
1. **Sales Trend Analysis** - Monthly sales performance tracking
2. **Location Performance** - Sales comparison across store locations (Hell's Kitchen, Astoria, Lower Manhattan)
3. **Product Category Mix** - Revenue distribution by product categories
4. **Product Performance** - Top-selling products and product types analysis

### Dynamic Filtering
- Date range selector
- Location-based filtering
- Product category and type filters

## 📁 Repository Structure

```
coffee-shop-dashboard/
├── README.md
├── data/
│   └── coffee_shop_transactions.xlsx
├── dashboard/
│   └── Coffee_Shop_Sales_Dashboard.pbix
├── images/
│   └── dashboard-preview.png
├── dax-measures/
│   └── measures.txt
```

## 🛠️ Technical Implementation

### Data Model
- **Data Source**: Excel file with transaction records
- **Key Tables**: Transactions table with proper relationships
- **Data Types**:
  - `transaction_id`, `transaction_qty`, `store_id`, `product_id` → Whole Numbers
  - `transaction_date` → Date
  - `transaction_time` → Time
  - `unit_price` → Decimal Number
  - `product_category`, `product_type`, `product_detail`, `store_location` → Text

### DAX Measures

```dax
Total Sales = SUMX(Transactions, Transactions[transaction_qty] * Transactions[unit_price])

Total Orders = DISTINCTCOUNT(Transactions[transaction_id])

Total Items = SUM(Transactions[transaction_qty])

Avg Order Value = DIVIDE([Total Sales], [Total Orders])

Items per Order = DIVIDE([Total Items], [Total Orders])
```

### Design Theme
- **Color Palette**: Coffee-inspired browns and beiges
- **Layout**: Grid-based responsive design
- **Typography**: Clean, professional fonts
- **Background**: Light beige with brown accents

## 📈 Key Business Insights

### 🏆 Performance Highlights
- **Revenue Leader**: Hell's Kitchen dominates with 236K in sales, significantly outperforming other locations
- **Average Transaction**: $4.69 per order indicates premium coffee positioning
- **Volume Efficiency**: 214K items across 149K orders = 1.44 items per transaction (opportunity for upselling)
- **Market Position**: 698.81K total revenue demonstrates strong market presence

### 🌟 Top Product Performance
| Product | Sales Volume | Market Impact |
|---------|-------------|---------------|
| Sustainably Grown Organic Lg | $21,151.75 | Clear customer preference for premium, eco-friendly options |
| Sustainably Grown Organic Rg | $16,233.75 | Strong demand across size variants |
| Traditional Blend Chai Lg | $12,522.00 | Tea category showing solid performance |
| Traditional Blend Chai Rg | $11,280.00 | Consistent chai demand |

### 📊 Category Analysis
- **Coffee Dominance**: Coffee products lead revenue generation (67.07% market share - 196.41K)
- **Tea Growth**: Traditional chai blends show strong secondary performance
- **Premium Focus**: "Premium brew" and "Scone" categories demonstrate successful premium positioning

### 🏪 Location Intelligence
1. **Hell's Kitchen** (236K): Premium location with highest foot traffic and sales
2. **Astoria** (232K): Nearly matching Hell's Kitchen - untapped potential for optimization
3. **Lower Manhattan** (230K): Consistent performance across all locations indicates strong brand presence

### 📈 Trend Analysis
- **Seasonal Patterns**: June data shows sales fluctuation from 5.8K to 6.4K, indicating demand volatility
- **Peak Performance**: Mid-month sales spike suggests promotional effectiveness or payroll-driven purchasing
- **Recovery Trends**: Sales recovery after dips shows resilient customer base

### 💡 Strategic Recommendations

#### Revenue Optimization
- **Upselling Opportunity**: With only 1.44 items per order, implement combo deals to increase basket size
- **Location Strategy**: Leverage Hell's Kitchen success model for Astoria and Lower Manhattan improvements
- **Premium Push**: 72.42K in premium segments shows customer willingness to pay for quality

#### Product Strategy
- **Organic Expansion**: Sustainably grown products are clear winners - expand this line
- **Size Optimization**: Large sizes outperform regular - consider promotional focus on larger portions
- **Cross-Category**: Strong chai performance suggests diversification opportunities in tea/alternative beverages

#### Operational Insights
- **Inventory Focus**: Top 5 products generate significant portion of revenue - ensure consistent stock
- **Staff Training**: Premium product positioning requires knowledgeable staff for effective upselling
- **Marketing**: Sustainability messaging resonates with customers based on organic product success

### 🎯 KPI Benchmarking
| Metric | Current Performance | Industry Standard | Status |
|--------|-------------------|-------------------|---------|
| Average Order Value | $4.69 | $4.50-$6.00 | ✅ Competitive |
| Items per Transaction | 1.44 | 1.6-2.0 | ⚠️ Below Target |
| Location Performance Variance | 2.6% | <5% | ✅ Excellent |
| Premium Product Share | 20.8% | 15-25% | ✅ Strong |

### 🔮 Growth Opportunities
1. **Bundling Strategy**: Create meal deals to increase items per order from 1.44 to target 2.0+
2. **Location Expansion**: Success across all 3 locations validates franchise/expansion potential
3. **Sustainability Marketing**: Organic products' success suggests eco-conscious branding opportunity
4. **Digital Integration**: Consistent performance indicates ready market for loyalty programs/app integration

## 🚀 Getting Started

### Prerequisites
- Microsoft Power BI Desktop (Latest version)
- Excel 2016 or later (for data source)

### Installation Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/coffee-shop-dashboard.git
   cd coffee-shop-dashboard
   ```

2. **Open Power BI File**
   - Launch Power BI Desktop
   - Open `Coffee_Shop_Sales_Dashboard.pbix`

3. **Update Data Source**
   - Go to Transform Data
   - Update file path to your local data file location
   - Refresh the data

4. **Publish to Power BI Service** (Optional)
   - Sign in to Power BI Service
   - Click "Publish" in Power BI Desktop
   - Select workspace destination

## 📊 Data Requirements

### File Format
- Excel (.xlsx) or CSV format
- Required columns:
  - transaction_id
  - transaction_date
  - transaction_time
  - transaction_qty
  - unit_price
  - store_id
  - product_id
  - product_category
  - product_type
  - product_detail
  - store_location

### Data Quality
- No missing values in key fields
- Proper date/time formatting
- Consistent text formatting for categories

## 🔧 Customization

### Adding New Measures
1. Go to Model view
2. Select table and click "New measure"
3. Add your DAX formula
4. Format as needed

### Modifying Visuals
1. Select visual in report view
2. Use Visualizations pane to modify
3. Apply consistent color theme

### Updating Filters
1. Select slicer visual
2. Modify field selection
3. Adjust formatting and layout

## 📱 Mobile Optimization

The dashboard is optimized for mobile viewing with:
- Responsive card layouts
- Touch-friendly filters
- Simplified mobile-specific views

## 🙏 Acknowledgments

- Power BI Community for inspiration
- Coffee shop industry data standards
- Microsoft Power BI documentation

---

**Built with ❤️ and ☕ using Microsoft Power BI**

*Last updated: August 29, 2025*
