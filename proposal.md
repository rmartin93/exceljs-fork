# 🚀 ExcelJS Community Fork - Fixing Critical Bugs & Looking for Maintainers

Hello everyone!

I've never needed to fork a library before to fix something, but **ExcelJS appears to be unmaintained** despite having active community usage and issues.

## 🐛 **Why I Forked**

I discovered a critical bug when working with Excel table templates:

1. **Load an Excel file** with a table using `workbook.xlsx.readFile()`
2. **Get the table** using `worksheet.getTable('TableName')`
3. **Try to add rows** using `table.addRow([data])`
4. **💥 CRASH**: `Cannot read properties of undefined (reading 'length')`

This affects anyone trying to:

-   ✅ Load existing Excel templates with tables
-   ✅ Add data to those tables programmatically
-   ✅ Preserve Excel table features (filters, totals, formatting)

## 🔧 **What I Fixed**

The fix turned out to be several compatibility issues between how Excel stores tables vs how ExcelJS expects them:

-   **Missing worksheet references** in loaded tables
-   **Excel format incompatibilities** (`tableRef` vs `ref` mapping)
-   **Filter button preservation** (autoFilter range calculation)
-   **Dynamic table expansion** when adding rows

## 📦 **My Fork**

**Repository**: https://github.com/rmartin93/exceljs-fork
**Status**: ✅ Bug fixed, ✅ Tests passing, ✅ 100% API compatible

## 🤝 **Looking for Community Support**

Since the original maintainer has been inactive, I'm considering:

1. **Publishing to NPM** as a community fork
2. **Taking on active maintenance**
3. **Building a contributor team**

### 🙋‍♂️ **How You Can Help**

-   **⭐ Star the repo** if this fix helps you
-   **🧪 Test with your use cases** - report any issues
-   **📝 Help with documentation**
-   **🐛 Report other bugs** you've encountered
-   **🔧 Submit PRs** for fixes or improvements
-   **💬 Spread the word** to others using ExcelJS

### 🎯 **Immediate Next Steps**

If there's community interest, and others will help, we could:

-   [ ] Publish to NPM
-   [ ] Set up proper issue templates & contributing guidelines
-   [ ] Create a roadmap for other known issues
-   [ ] Establish a release schedule

## 💭 **Questions for the Community**

1. **Are you currently blocked** by ExcelJS bugs?
2. **Would you switch** to a community-maintained fork?
3. **What other issues** should we prioritize?
4. **Are you interested** in contributing?

Let's keep this excellent library alive! 🚀

---

_Note: This is meant to complement, not compete with the original ExcelJS. If the original maintainer returns, I'm happy to merge efforts._

---

_Full Disclosure: I did have AI help me write this out to make it look more polished than it would have if I wrote it myself. I'd rather have the original maintainer merge the changes I made, and the one's I've seen the community working on / asking for. However, I am open to helping if I can._
