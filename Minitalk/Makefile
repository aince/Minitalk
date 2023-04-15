# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: aince <aince@student.42kocaeli.com.tr>     +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/03/20 13:46:26 by aince             #+#    #+#              #
#    Updated: 2023/03/24 12:38:15 by aince            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CFLAGS = -Wall -Werror -Wextra
CLIENT= @$(CC) $(CFLAGS) client.c ft_printf.c -o $(NAME_CL)
SERVER= @$(CC) $(CFLAGS) server.c ft_printf.c -o $(NAME_SV)
NAME_CL = client
NAME_SV = server


all: $(NAME_CL) $(NAME_SV)
$(NAME_CL):
	$(CLIENT)
$(NAME_SV):
	$(SERVER)
clean:
	@rm -rf client server
	@echo "\n\033[42m object files removed 👋\033[0m\n"
norm:
	norminette *.c *.h
run:
	@make
	./server
fclean: clean
	@echo "\n\033[42m executables removed 👋\033[0m\n"
	@rm -rf client.o server.o
re: clean all
.PHONY: all bonus clean fclean re