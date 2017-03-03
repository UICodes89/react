# reactReact application Installation
	-npm install -g babel
	-npm init
	-npm install webpack --save
	-npm install webpack-dev-server --save
	-npm install react --save
	-npm install react-dom --save
	-npm install babel-core
	-npm install babel-loader
	-npm install babel-preset-react
	-npm install babel-preset-es2015
	  -index.html
	  -App.jsx
	  -main.js
	  -webpack.config.js
	  		var config = {
			   entry: './main.js',
				
			   output: {
			      path:'./',
			      filename: 'index.js',
			   },
				
			   devServer: {
			      inline: true,
			      port: 8080
			   },
				
			   module: {
			      loaders: [
			         {
			            test: /\.jsx?$/,
			            exclude: /node_modules/,
			            loader: 'babel',
							
			            query: {
			               presets: ['es2015', 'react']
			            }
			         }
			      ]
			   }
			}

			module.exports = config;
