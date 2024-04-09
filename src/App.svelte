<script>
  let currencies = [
    {
      moneda: "BTC",
      value: 69350.08,
      ratio: -1.0900
    },
    {
      moneda: "ETH",
      value: 2350.67,
      ratio: 0.7600
    },
    {
      moneda: "LTC",
      value: 182.54,
      ratio: 2.1500
    }
  ];
</script>


<h2 class="title">Lista de Monedas</h2>
<ul>
  {#each currencies as currency}
    <li>
      <div class="currency-info">
        {currency.moneda}
        <div class="values">
          <span>${currency.value}</span>
          <span style="color: {currency.ratio > 0 ? 'green' : 'red'}">
            {currency.ratio > 0 ? '+' : ''}{currency.ratio}%
          </span>
        </div>
        
        
    </li>
  {/each}
</ul>

<style>
  ul {
    list-style: none;
    padding: 0;
  }
  
  li {
    margin-bottom: 20px;
    padding: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .currency-info {
    display: flex;
    justify-content: space-between;
    font-weight: bold;
    margin-bottom: 10px;
    align-items: center;
  }
  
  .values {
    display: flex;
    flex-direction: column;
    align-items: center;
  }


  
  .title {
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 20px;
  }
</style>
