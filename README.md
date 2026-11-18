# ataques-de-for-a-bruta.

import itertools


senha_nova = "mar"
hash_novo = calcula_hash(senha_nova)


caracteres = "abcdefghijklmnopqrstuvwxyzABC123!@#$"

print(f"Iniciando força bruta para uma senha de {len(senha_nova)} caracteres...")


for combinacao_tupla in itertools.product(caracteres, repeat=len(senha_nova)):
    # O product retorna uma tupla de caracteres, precisamos juntá-los em uma string
    tentativa = "".join(combinacao_tupla)
    
    # Comparamos o hash da tentativa com o hash alvo
    if calcula_hash(tentativa) == hash_novo:
        print(f"Senha encontrada: {tentativa}")
        break
        import bcrypt


senha_original = "minha_senha_super_secreta_123"


senha_bytes = senha_original.encode('utf-8')



hashed_senha = bcrypt.hashpw(senha_bytes, bcrypt.gensalt())

print(f"Hash armazenado no banco de dados:\n{hashed_senha}\n")


tentativa_correta = "minha_senha_super_secreta_123"
if bcrypt.checkpw(tentativa_correta.encode('utf-8'), hashed_senha):
    print("✅ Login realizado com sucesso! (Senha correta)")
else:
    print("❌ Acesso negado. (Senha incorreta)")


tentativa_errada = "senha_errada"
if bcrypt.checkpw(tentativa_errada.encode('utf-8'), hashed_senha):
    print("✅ Login realizado com sucesso!")
else:
    print("❌ Acesso negado. (Senha incorreta detectada com segurança)")
    import bcrypt

senha = "minha_senha_super_secreta"
senha_bytes = senha.encode('utf-8')


custo_personalizado = 14


hashed_com_custo = bcrypt.hashpw(senha_bytes, bcrypt.gensalt(rounds=custo_personalizado))

print(hashed_com_custo)
    
