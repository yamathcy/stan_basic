
// 単回帰モデルをstanにより実行する
data {
  int N;
  real X[N];
  real Y[N];
}

// 単回帰で推定すべきは回帰係数，切片とノイズが従う正規分布の標準偏差σ
parameters {
  real a;
  real b;
  real <lower=0> sigma;
  
}

model {
  for (n in 1:N){
  Y[n] ~ normal(a + b*X[n], sigma);
  }
}

