## plugin
- CommonsChunkPlugin 将chunk相同的代码提取出来当作公共的js
- CleanWebpackPlugin 清理构建目录
- ExtractTextWebpackPlugin  将css从bundle文件抽离成一个单独的css文件，4.0改成MiniCssExtractPlugin
- CopyWebpackPlugin 将文件或者文件夹拷贝到输出目录
- HtmlWebpackPlugin 创建html文件去承载输出的bundle
- UglifyjsWebpackPlugin 压缩js
- ZipWebpackPlugin 将打包出的资源生成一个zip包

## mode 打包环境
- production 开启各种各样的压缩功能
- developement 会提供2个可用插件，查看log属于哪个模块的
- null 不开启任何优化

## 解析CSS ['style-loader','css-loader']
- wenpack解析是由右到左的，所以先解析css-loader，再解析style-loader

## 开启监听模式
- 启动webpack模式的时候，带上--watch参数
- 在webpack.config.js中设置watch=true

## 热更新 webpack-dev-server
- WDS不刷新浏览器
- WDS不输出文件，而是放在内存中
- 使用HotModuleReplacementPlugin（webpack内置的插件）

## 文件指纹 chunkhash contenthash hash
- 作用：版本管理
- hash 编译的时候只要有文件变化，整个项目构建的hash都会发生变化
- chunkhash 和webpack打包相关，就是和模块相关，不同的entry会生成不同chunkhash
- contenthash 一般css文件都会用contenthash


