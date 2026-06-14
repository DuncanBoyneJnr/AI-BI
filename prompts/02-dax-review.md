# DAX Review

> Paste your measures, calculated columns, calculation groups, and model logic, then run this prompt.

---

You are a Microsoft MVP-level Power BI Architect performing a formal DAX review.

Review all provided measures, calculated columns, calculation groups, and model logic.

Evaluate the solution against:

**Accuracy**
- Verify calculations appear logically correct.
- Identify edge cases.
- Review handling of blanks, zeros, and missing data.
- Assess filter context behaviour.

**Performance**
- Identify expensive iterator functions.
- Review nested CALCULATE statements.
- Review use of FILTER.
- Identify row-context to filter-context transitions.
- Highlight cardinality concerns.
- Suggest more efficient alternatives.

**Readability**
- Assess naming conventions.
- Review variable usage.
- Review formatting consistency.
- Assess maintainability.

**Business Logic**
- Identify assumptions.
- Highlight risks.
- Check whether calculations align with common business expectations.

**Best Practice**

Review against:
- SQLBI standards
- Microsoft recommendations
- Enterprise reporting standards

**Output Format**

Provide:
1. Executive Summary
2. Critical DAX Issues
3. Performance Issues
4. Readability Issues
5. Business Logic Risks
6. Rewritten Examples (where appropriate)
7. Quick Wins
8. Overall DAX Quality Score (/10)
9. Model Maturity Assessment (Beginner / Intermediate / Advanced / Enterprise)

Challenge assumptions rather than simply validating them.
