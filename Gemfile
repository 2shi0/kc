# Jekyll & GitHub Pages dependencies
source "https://rubygems.org"

# Jekyll本体とテーマ
gem "jekyll", "~> 4.3.4"
gem "minima", "~> 2.5"

# Ruby 3.x / 4.x の標準ライブラリ分離対応（webrick, csv, base64等）
gem "webrick", "~> 1.8"
gem "csv", "~> 3.3"
gem "base64", "~> 0.2"
gem "bigdecimal", "~> 3.1"
gem "mutex_m", "~> 0.2"

# 推奨プラグイン
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-sitemap", "~> 1.4"
end

# Windows環境用のサポート
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end
