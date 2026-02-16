# Tax Strategist

Expert tax planning agent that develops tax-efficient strategies, identifies deductions, optimizes entity structures, and ensures compliance. Specializes in small business taxation, founder/entrepreneur tax planning, and strategic tax minimization.

This skill applies tax planning principles to legally minimize tax burden while ensuring compliance with tax laws. Perfect for LLC/S-Corp decisions, quarterly tax planning, deduction optimization, and year-end tax strategies.

**Disclaimer:** This skill provides educational tax guidance. Always consult a qualified CPA or tax attorney for specific tax advice and filing.

## Connection to Tax Savings Agent Subagents

When implementing, refining, or debugging **any Tax Savings Agent execution subagent**, use this skill for domain logic, workflows, and compliance. Each core workflow below maps to a specific subagent in the Tax Savings Agent architecture:

| Subagent | Tax Strategist workflow(s) | Use this skill for |
|----------|---------------------------|---------------------|
| **Entity Agent** | Workflow 1: Entity Structure Optimization | S-Corp/LLC analysis, reasonable salary, election timing, state filing |
| **Deduction Agent** | Workflow 2: Deduction Maximization | Expense categories, home office, vehicle, retirement, QBI, depreciation |
| **TLH Agent** | Workflow 6: Tax Loss Harvesting | Lot selection, wash sale rules, replacement securities, savings calc |
| **Quarterly / Payments Agent** | Workflow 3: Quarterly Tax Planning | Estimated taxes, safe harbor, payment schedule, penalty avoidance |
| **Year-End / Timing Agent** | Workflow 4: Year-End Tax Strategies | Income/expense timing, deferral/acceleration, retirement deadlines |
| **Compliance / Audit Agent** | Workflow 5: Tax Audit Preparation | Documentation, risk triggers, audit defense, record retention |

**When to invoke this skill:** Any task involving Tax Savings Agent subagent specs, prompts, tools, or user flows for Entity, Deduction, TLH, Quarterly, Year-End, or Audit/Compliance—read the corresponding workflow(s) above and apply the steps, formulas, and reference tables in this skill.

## Core Workflows

### Workflow 1: Entity Structure Optimization

**Objective:** Determine optimal business entity structure for tax efficiency

**Steps:**

1. **Current Situation Analysis**  
   * Current entity type (sole prop, LLC, S-Corp, C-Corp)  
   * Annual revenue and net income  
   * Owner compensation  
   * Number of owners/members  
   * State of operation  
   * Growth trajectory

2. **Entity Comparison Analysis**  
**Sole Proprietorship / Single-Member LLC (Disregarded):**  
   * Pass-through taxation  
   * Self-employment tax on all net income (15.3%)  
   * Simple administration  
   * Limited liability protection (LLC only)  
   * Best for: Low income, simplicity priority  

**LLC with S-Corp Election:**  
   * Pass-through taxation  
   * Self-employment tax only on wages  
   * Reasonable salary requirement  
   * Payroll administration required  
   * Best for: Net income > $40-50K after salary  

**C-Corporation:**  
   * Double taxation (corporate + dividend)  
   * 21% flat corporate rate  
   * Ability to retain earnings  
   * Fringe benefit deductions  
   * Best for: High growth, reinvesting profits, or planning IPO

3. **S-Corp Savings Calculation**  
```
Current (Schedule C):
Net Income: $150,000
Self-Employment Tax: $150,000 × 15.3% = $22,950

With S-Corp Election:
Reasonable Salary: $80,000
Payroll Taxes: $80,000 × 15.3% = $12,240
Distribution: $70,000 (no SE tax)
Annual Savings: $22,950 - $12,240 = $10,710
```

4. **Reasonable Salary Determination**  
   * Industry standards for role  
   * Geographic location factors  
   * Experience and qualifications  
   * Company profitability  
   * IRS guidelines (typically 60-80% of net income initially)

5. **Implementation Considerations**  
   * State filing requirements  
   * Election timing (S-Corp: within 75 days of tax year)  
   * Payroll setup requirements  
   * Accounting complexity increase  
   * Ongoing compliance costs

6. **Recommendation**  
   * Recommended entity structure  
   * Estimated annual tax savings  
   * Implementation steps  
   * Timing considerations  
   * Professional referrals needed

**Deliverable:** Entity structure analysis with tax savings estimate

### Workflow 2: Deduction Maximization

**Objective:** Identify all available deductions to minimize taxable income

**Steps:**

1. **Business Expense Review**  
**Ordinary & Necessary Deductions:**  
   * Office supplies and equipment  
   * Software and subscriptions  
   * Professional services (legal, accounting)  
   * Marketing and advertising  
   * Travel, meals (50% deductible), lodging  
   * Education and training  
   * Bank fees and interest  
   * Insurance premiums  

**Home Office Deduction:**  
   * Dedicated workspace required  
   * Regular and exclusive use  
   * Simplified method: $5/sq ft (max $1,500)  
   * Actual expense method: Proportional share  
   * Includes: mortgage/rent, utilities, insurance, repairs  

**Vehicle Expenses:**  
   * Standard mileage: 67 cents/mile (2024)  
   * Actual expenses: gas, insurance, repairs, depreciation  
   * Business use percentage required  
   * Mileage log recommended

2. **Retirement Contributions**  
| Plan Type       | 2024 Limit                           | Notes                 |
| --------------- | ------------------------------------ | --------------------- |
| SEP-IRA         | 25% of net SE income (max $69,000)   | Simple, employer-only |
| Solo 401(k)     | $23,000 + 25% employer (max $69,000) | Employee + employer   |
| SIMPLE IRA      | $16,000 + 3% match                   | Lower limits          |
| Defined Benefit | Actuarially determined               | Highest limits        |

3. **Health-Related Deductions**  
   * Self-employed health insurance deduction (100%)  
   * HSA contributions ($4,150 individual / $8,300 family)  
   * Long-term care insurance premiums (age-based limits)

4. **Section 199A (QBI) Deduction**  
   * 20% of Qualified Business Income  
   * Subject to income limits ($191,950 single / $383,900 MFJ)  
   * SSTB limitations at high income  
   * W-2 wage and property limitations  
   * Optimal structuring strategies

5. **Depreciation Strategies**  
   * Section 179 expensing ($1,220,000 limit)  
   * Bonus depreciation (60% in 2024)  
   * Standard depreciation schedules  
   * Vehicles: $12,200 first year (+ bonus)  
   * Listed property rules

6. **Often Overlooked Deductions**  
   * State and local taxes (up to $10,000)  
   * Charitable contributions  
   * Student loan interest  
   * Business use of cell phone  
   * Business-related books/publications  
   * Professional memberships  
   * Bad debt write-offs

**Deliverable:** Comprehensive deduction checklist with estimated savings

### Workflow 3: Quarterly Tax Planning

**Objective:** Optimize estimated tax payments and year-round tax planning

**Steps:**

1. **Income Projection**  
   * Year-to-date income  
   * Projected remaining income  
   * One-time income events  
   * Quarterly income timing

2. **Tax Liability Estimation**  
   * Federal income tax brackets  
   * Self-employment tax  
   * State income tax  
   * Local taxes (if applicable)

3. **Safe Harbor Calculation**  
   * 100% of prior year tax (110% if AGI > $150K)  
   * OR 90% of current year tax  
   * Choose method to minimize payments

4. **Quarterly Payment Schedule**  
| Quarter | Period         | Due Date     |
| ------- | -------------- | ------------ |
| Q1      | Jan 1 - Mar 31 | April 15     |
| Q2      | Apr 1 - May 31 | June 15      |
| Q3      | Jun 1 - Aug 31 | September 15 |
| Q4      | Sep 1 - Dec 31 | January 15   |

5. **Cash Flow Optimization**  
   * Minimum required payments  
   * Penalty avoidance strategies  
   * Year-end catch-up options  
   * Underpayment penalty calculation

6. **Mid-Year Adjustments**  
   * Income variance analysis  
   * Deduction timing strategies  
   * Entity structure changes  
   * Retirement contribution adjustments

**Deliverable:** Quarterly estimated tax payment schedule

### Workflow 4: Year-End Tax Strategies

**Objective:** Implement year-end strategies to minimize current year taxes

**Steps:**

1. **Income Analysis**  
   * YTD actual income  
   * Remaining expected income  
   * Marginal tax bracket  
   * Comparison to prior year

2. **Income Deferral Strategies**  
   * Delay invoicing to next year  
   * Defer receipt of payments  
   * Installment sales treatment  
   * Defer bonuses (employees)

3. **Income Acceleration Strategies** (When next year will be higher income)  
   * Accelerate billing  
   * Recognize deferred revenue  
   * Roth conversions  
   * Capital gain harvesting

4. **Expense Acceleration**  
   * Prepay deductible expenses  
   * Purchase equipment (Section 179)  
   * Maximize retirement contributions  
   * Pay Q1 state taxes in December  
   * Stock up on supplies

5. **Expense Deferral** (When next year will be higher income)  
   * Delay discretionary purchases  
   * Postpone major repairs  
   * Defer prepayments

6. **Retirement Contribution Maximization**  
   * Calculate max contribution room  
   * Deadline awareness:  
     * 401k employee: December 31  
     * SEP/401k employer: Tax filing deadline  
   * Catch-up contributions (50+)

7. **Capital Gains/Losses**  
   * Tax-loss harvesting  
   * Long-term vs short-term optimization  
   * Wash sale rules (30 days)  
   * Charitable donation of appreciated assets

8. **Charitable Giving Strategies**  
   * Bunching deductions  
   * Donor-advised funds  
   * Qualified Charitable Distributions (70.5+)  
   * Appreciated asset donations

**Deliverable:** Year-end tax action plan with savings estimate

### Workflow 5: Tax Audit Preparation

**Objective:** Prepare for potential tax audit and minimize risk

**Steps:**

1. **Audit Risk Assessment**  
   * High-risk triggers:  
     * Large deductions relative to income  
     * Home office deduction  
     * Vehicle deductions  
     * Cash-intensive business  
     * High Schedule C income  
     * Previous audit history

2. **Documentation Review**  
   * Income verification (1099s, bank statements)  
   * Expense receipts and invoices  
   * Mileage logs  
   * Home office measurements  
   * Asset purchase documentation  
   * Contractor 1099s issued

3. **Record Organization**  
   * Chronological expense files  
   * Bank statement reconciliation  
   * Credit card statement backup  
   * Digital backup system  
   * 7-year retention policy

4. **Audit Defense Preparation**  
   * Understand audit types:  
     * Correspondence audit (mail)  
     * Office audit (IRS office)  
     * Field audit (your location)  
   * Know your rights  
   * Representation options (CPA, EA, attorney)

5. **Common Audit Issues**  
   * Mixed personal/business expenses  
   * Insufficient documentation  
   * Hobby loss rules  
   * Contractor vs employee classification  
   * Unreported income

**Deliverable:** Audit readiness checklist and documentation guide

### Workflow 6: Tax Loss Harvesting (Proactive Investment Optimization)

**Objective:** Proactively identify and execute tax-loss harvesting opportunities to offset capital gains and reduce taxable income

**Steps:**

1. **Portfolio Analysis**  
   * Current holdings with cost basis (per lot)  
   * Unrealized gains and losses by position  
   * YTD realized capital gains (short-term vs long-term)  
   * Capital loss carryforward from prior years  
   * Current marginal tax rate and capital gains rate

2. **Opportunity Identification**  
   * Positions with unrealized losses > $500 threshold  
   * Short-term vs long-term loss classification  
   * Optimal lot selection (highest cost basis first = largest loss)  
   * Priority order:
     - Short-term losses (offset short-term gains at ordinary rates)
     - Long-term losses (offset long-term gains at preferential rates)
     - $3,000 ordinary income offset (if no gains to offset)

3. **Savings Calculation**  
```
Tax-Loss Harvesting Savings Formula:
═══════════════════════════════════════════════════════════════
IF short-term gains available:
  Savings = Loss harvested × Marginal tax rate (e.g., 24%)

IF only long-term gains available:
  Savings = Loss harvested × Capital gains rate (0%, 15%, 20%)

IF no gains available:
  Savings = MIN(Loss, $3,000) × Marginal tax rate
  Carryforward = Loss - $3,000 (for future years)

Example:
  $5,000 short-term loss × 24% marginal rate = $1,200 tax savings
  $5,000 long-term loss × 15% cap gains rate = $750 tax savings
```

4. **Wash Sale Prevention**  
   * **30-day lookback**: Check if same security purchased in prior 30 days  
   * **30-day lookahead**: Avoid repurchasing within 30 days after sale  
   * **Substantially identical securities**: Same stock, options, mutual funds tracking same index  
   * **Cross-account monitoring**: IRA, 401(k), and spouse accounts count!  
   * **Total window**: 61 days (30 before + sale day + 30 after)

5. **Replacement Security Selection**  
   * Similar sector/asset class exposure (NOT substantially identical)  
   * Common replacements:
     - VTI → SCHB or ITOT (US total market)
     - SPY → IVV or VOO (S&P 500) — Note: These may be substantially identical
     - QQQ → QQQM or VGT (tech exposure)
     - Individual stock → Sector ETF (AAPL → XLK)
   * ETF alternatives for mutual funds  
   * Set 31-day repurchase calendar reminder

6. **Execution Plan**  
   * Specific lots to sell with cost basis documentation  
   * Expected tax savings calculation  
   * Replacement securities to purchase  
   * Wash sale safe date for original security repurchase  
   * Year-end consideration: Allow T+2 settlement before Dec 31

**Proactive Triggers:**
* Market decline > 5% in 30 days
* Individual position loss > $500
* October-December (year-end optimization window)
* YTD realized gains exceed $5,000 (offset opportunity)

**Deliverable:** Tax-loss harvesting action plan with lot selection, replacement securities, and wash sale calendar

## Quick Reference

| Action              | Command/Trigger                     |
| ------------------- | ----------------------------------- |
| Entity analysis     | "Should I elect S-Corp status?"     |
| Deductions          | "What deductions am I missing?"     |
| Quarterly taxes     | "Calculate my estimated taxes"      |
| Year-end planning   | "Year-end tax strategies"           |
| Retirement planning | "Maximize retirement contributions" |
| Tax projection      | "Project my tax liability"          |
| Tax loss harvesting | "Harvest my investment losses"      |
| Wash sale check     | "Can I repurchase [security]?"      |
| TLH opportunities   | "What losses can I harvest?"        |

## Tax Rate Reference (2024)

### Federal Income Tax Brackets (Single)

| Taxable Income      | Rate |
| ------------------- | ---- |
| $0 - $11,600        | 10%  |
| $11,601 - $47,150   | 12%  |
| $47,151 - $100,525  | 22%  |
| $100,526 - $191,950 | 24%  |
| $191,951 - $243,725 | 32%  |
| $243,726 - $609,350 | 35%  |
| $609,351+           | 37%  |

### Self-Employment Tax

* Social Security: 12.4% (up to $168,600 for 2024)
* Medicare: 2.9% (no cap)
* Additional Medicare: 0.9% (income over $200K single)
* Total: 15.3% (+ 0.9% high income)
* 50% is deductible as adjustment to income

### Capital Gains Tax (2024)

| Rate | Single Income      | MFJ Income         |
| ---- | ------------------ | ------------------ |
| 0%   | Up to $47,025      | Up to $94,050      |
| 15%  | $47,026 - $518,900 | $94,051 - $583,750 |
| 20%  | Over $518,900      | Over $583,750      |

### Wash Sale Rules (IRC §1091)

The wash sale rule prevents claiming a loss on a security if you purchase a "substantially identical" security within 30 days before or after the sale.

**Key Rules:**
* **61-day window**: 30 days before + sale day + 30 days after
* **Substantially identical**: Same stock, same class, options on same stock, mutual funds/ETFs tracking same index
* **Cross-account**: Applies across ALL accounts—brokerage, IRA, 401(k), spouse accounts
* **Disallowed loss**: Added to cost basis of replacement security (deferred, not lost)
* **Holding period**: Replacement security inherits original holding period

**Common Wash Sale Traps:**
| Action | Wash Sale? |
| ------ | ---------- |
| Sell VTI, buy SCHB next day | No (different fund, similar exposure) |
| Sell VTI, buy VTI in IRA within 30 days | Yes (IRA counts) |
| Sell AAPL, buy AAPL call option within 30 days | Yes (options count) |
| Spouse sells VTI, you buy VTI within 30 days | Yes (spouse counts) |
| Sell VTSAX mutual fund, buy VTI ETF within 30 days | Unclear (both track same index—conservative: avoid) |

**Tax-Loss Harvesting Replacement Pairs:**
| Security | Non-Identical Replacement |
| -------- | ------------------------- |
| VTI (Vanguard Total Market) | SCHB (Schwab), ITOT (iShares) |
| SPY (S&P 500) | IVV (iShares), VOO (Vanguard) |
| QQQ (Nasdaq 100) | QQQM (Invesco), VGT (Vanguard Tech) |
| AGG (Total Bond) | BND (Vanguard), SCHZ (Schwab) |
| Individual stocks | Sector ETF (e.g., AAPL → XLK) |

## Deduction Cheat Sheet

```markdown
## Common Business Deductions

### Fully Deductible (100%)
- [ ] Advertising and marketing
- [ ] Bank fees and interest
- [ ] Business insurance
- [ ] Contract labor
- [ ] Education (business-related)
- [ ] Legal and professional fees
- [ ] Office supplies
- [ ] Rent (business property)
- [ ] Software and subscriptions
- [ ] Telephone and internet (business %)
- [ ] Travel (business purpose)

### Partially Deductible
- [ ] Meals (50%)
- [ ] Vehicle (business % or mileage)
- [ ] Home office (business % of home)
- [ ] Cell phone (business % of usage)
- [ ] Entertainment (0% - not deductible since 2018)

### Above-the-Line Deductions
- [ ] Self-employed health insurance (100%)
- [ ] SEP/SIMPLE/Solo 401k contributions
- [ ] 1/2 of self-employment tax
- [ ] Student loan interest (up to $2,500)
- [ ] HSA contributions
```

## Best Practices

### Year-Round

* Track all expenses in real-time
* Maintain separate business accounts
* Save 25-30% for taxes
* Make quarterly payments
* Keep receipts (digital backup)
* Monitor portfolio for tax-loss harvesting opportunities (especially in market downturns)
* Track wash sale windows across all accounts (brokerage, IRA, spouse)
* Prioritize harvesting short-term losses over long-term (higher tax benefit)

### Annually

* Review entity structure
* Maximize retirement contributions
* Implement year-end strategies
* Reconcile 1099s received
* File on time or extend
* Execute tax-loss harvesting before December settlement cutoff (mid-December)
* Review capital gains/losses and plan offsets before year-end
* Consider replacement securities before selling (avoid unintended wash sales)

### Documentation

* Keep 7 years of records
* Contemporaneous mileage log
* Written home office policy
* Detailed expense categorization
* Contractor agreements on file

## Common Pitfalls to Avoid

* **Missing estimated payments:** Penalties add up quickly
* **Commingling funds:** Keep business and personal separate
* **Ignoring state taxes:** State rules differ significantly
* **Aggressive deductions:** Red flags invite audits
* **Missing documentation:** No receipt = no deduction
* **Late S-Corp election:** Must file within 75 days
* **Incorrect contractor classification:** Misclassification penalties are severe
* **Ignoring nexus issues:** Multi-state operations create complexity
* **Wash sale violations:** Repurchasing substantially identical securities within 30 days disallows the loss
* **Missing TLH opportunities:** Market downturns are prime harvesting windows—don't wait until year-end
* **Cross-account wash sales:** IRA and spouse purchases count—track all accounts

## Disclaimer

This skill provides educational tax information only. Tax law is complex and varies by jurisdiction. Always:

* Consult a qualified CPA or tax attorney for specific advice
* Verify current tax rates and limits (they change annually)
* Consider your complete financial picture
* File accurately and on time
