# Investment Opportunity Analysis
*Project Objectives*

**⚡⚡Spark Funds⚡⚡**

**1. Project Brief**

Spark Funds is an asset management company. Spark Funds wants to make investments in a few companies. The CEO of Spark Funds wants to understand the global trends in investments so that she can take the investment decisions effectively.

**2. Business and Data Understanding**

Spark Funds has two minor constraints for investments:
- It wants to invest between 5 to 15 million USD per round of investment.
- It wants to invest only in English-speaking countries because of the ease of communication with the companies it would invest in.

**3. Strategy**

Spark Funds wants to invest where most other investors are investing.

**4. Business objective**

Identify the best sectors, countries, and a suitable investment type for making investments. The overall strategy is to invest where others are investing, implying that the 'best' sectors and countries are the ones 'where most investors are investing'.

**5. Data analysis objective** 

Divided into 3 sub-goals:
- Investment type analysis: Comparing the typical investment amounts in the venture, seed, angel, private equity etc. so that Spark Funds can choose the type that is best suited for their strategy.
- Country analysis: Identifying the countries which have been the most heavily invested in the past. These will be Spark Funds’ favourites as well.
- Sector analysis: Understanding the distribution of investments across the eight main sectors. (Note that we are interested in the eight 'main sectors' provided in the mapping file. The two files — 'companies' and 'rounds2' — have numerous sub-sector names; hence, you will need to map each sub-sector to its main sector.)

  <h2> Proposed approach </h2> 

A - Overall approach: 

I utilize descriptive analytics and alternative risk-return analysis with correlation to gain valuable insights.

B - About the dataset: 

In this analysis, I use 3 dataset: 'companies', 'rounds2', 'mapping'. Please view the dataset here:

*1. 'rounds2'*

- This dataset contains information about individual funding rounds for companies. Each record represents a single investment round for a specific company.

- Data Dictionary:

| Field Name  | Description	 | Data Type | Example |
| ------------- | ------------- | ------------- | ------------- |
| company_permalink  | Unique identifier for the company that received the funding  | String  | /organization/-fame  |
| funding_round_permalink  | Unique identifier for the specific funding round  | String  | /funding-round/9a01d05418af9f794eebff7ace91f638  |
| funding_round_type  | The type of funding round (e.g., seed, Series A, Series B, etc.)  | String  | venture  |
| funding_round_code  | A code representing the funding round type (may differ from funding_round_type)  | String  | B  |
| funded_at  | The date the funding round was completed  | String (format might need conversion)  | 5/1/2015  |
| raised_amount_usd  | The amount of money raised in the funding round in USD  | Integer  | 10000  |

*2. 'mapping'*

- This dataset contains a mapping between sub-sectors and their corresponding main sectors. It helps categorize companies based on their broader industry.
  
- Data dictionary: Binary Representation (0/1) (1 for belonging, 0 for not belonging)

*3. 'companies'*

-This dataset contains general information about the companies themselves.

- Data Dictionary:

| Field Name  | Description	 | Data Type | Example |
| ------------- | ------------- | ------------- | ------------- |
| permalink  | Unique identifier for the company  | String  | same as company_permalink in 'rounds2'  |
| name  | The official name of the company  | String  | Acme Inc  |
| homepage_url  | The company's website URL	 | String  | https://www.acmeinc.com  |
| category_list	 | A list of categories the company belongs to  | List of Strings	  | ["Software", "Cloud Computing"]  |
| status  | The current operational status of the company  | String  |operating  |
| country_code  | The two-letter ISO code for the country where the company is headquartered  | String  | US  |
| state_code  | The state or province code for the company's location  | String  | CA  |
| region  | The broader region within the country  | String  | Bay Area  |
| city  | The city where the company is headquartered  | String  | San Francisco  |
| founded_at  | The date the company was founded  | String (format might need conversion)	  | 2010-01-01  |

