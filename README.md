const express = require('express')
const rotaUsuario = require('./AULA 06 - API EXPRESS ROTAS/rotas/usuario.rota')
const rotaPost = require('./AULA 06 - API EXPRESS ROTAS/rotas/posts.rota')

const app = express()
app.use(express.json())

app.use('/usuarios', rotaUsuario)
app.use('/posts', rotaPost)



app.get('/', (req, res) => {
    res.json({msg: "Hello From Express!!"})
})



app.listen(8080, () => {
    console.log('Bem-vindos ao meu servidor rodando na porta 8080!!')
})
